MASTER PROMPT: Build an Enterprise-Grade Responsive Modal Component in React + TypeScript

Act as a Senior Frontend Architect with expertise in React, TypeScript, accessibility, reusable component libraries, design systems, and enterprise-level UI architecture.

I want you to design and implement a production-ready, reusable, responsive Modal component using React and TypeScript.

1. Core Requirements

* Use React with TypeScript.
* Use Compound Component Pattern.
* Use clean, scalable, reusable architecture.
* Do not use third-party modal or dialog libraries.
* Use React Portal for rendering the modal.
* Support dynamic content and dynamic footer actions.
* Follow SOLID principles and clean code practices.
* Ensure compatibility with React Strict Mode.

2. Expected API

The component should support this API:

<Modal
  isOpen={isOpen}
  onClose={handleClose}
  ariaLabel="User details"
  closeOnOverlayClick={true}
  closeOnEscape={true}
>
  <Modal.Header title="User Details" />
  <Modal.Content>
    <p>Dynamic modal content goes here.</p>
  </Modal.Content>
  <Modal.Footer>
    <button type="button">Cancel</button>
    <button type="button">Save</button>
    <button type="button">Submit</button>
  </Modal.Footer>
</Modal>

The footer must accept any number of buttons or custom React elements. Never hardcode the number of footer buttons.

3. Component Architecture

Implement the Compound Component Pattern:

* Modal (Root)
* Modal.Header
* Modal.Content
* Modal.Footer

Use Object.assign() or an equivalent strongly typed approach to expose subcomponents.

Use React Context where appropriate for shared modal functionality.

4. Accessibility Requirements

Follow WAI-ARIA dialog practices and WCAG 2.2 AA considerations.

Implement:

* role=“dialog”
* aria-modal=“true”
* Accessible dialog name using aria-labelledby or aria-label.
* aria-describedby when a description is provided.
* Keyboard navigation.
* Focus trapping inside the modal.
* Initial focus management.
* Focus restoration to the previously focused element.
* Escape key handling.
* Proper close button accessibility labels.
* Background interaction prevention while modal is open.
* Screen-reader-friendly semantic HTML.

Ensure the dialog always has an accessible name, even when Modal.Header is not provided.

5. Responsive Design

The modal must work properly on:

* Desktop
* Laptop
* Tablet
* Mobile

Requirements:

* Configurable width and maximum width.
* Responsive height and maximum height.
* Scrollable content area.
* Header and footer should remain appropriately positioned.
* On small screens, support a full-screen or bottom-sheet presentation.
* Prevent horizontal overflow.
* Support CSS media queries.
* Support prefers-reduced-motion.

6. Advanced Functionality

Implement:

* React Portal.
* Body scroll locking.
* Overlay click handling.
* Escape key handling.
* Focus trapping and restoration.
* Dynamic footer content.
* Optional close icon.
* Optional header and footer.
* Configurable modal size.
* Custom className and styling support.
* Safe cleanup of event listeners and DOM changes.
* SSR-safe handling of document and window.
* Correct behavior in React Strict Mode.

Consider nested modals and multiple modal instances. Explain any limitations if full support requires a modal manager.

7. Code Quality

* Use strict TypeScript types.
* Avoid any.
* Avoid unnecessary useEffect hooks.
* Avoid prop drilling where Context is more appropriate.
* Use reusable utility functions.
* Separate component logic and styling.
* Ensure proper cleanup.
* Avoid memory leaks.
* Follow React best practices.
* Add meaningful comments only where necessary.

8. Suggested Folder Structure

Modal/
├── Modal.tsx
├── Modal.types.ts
├── ModalContext.ts
├── ModalHeader.tsx
├── ModalContent.tsx
├── ModalFooter.tsx
├── Modal.css
├── utils/
│   ├── focusTrap.ts
│   └── modalManager.ts
├── __tests__/
│   ├── Modal.test.tsx
│   └── Modal.accessibility.test.tsx
└── index.ts

You may improve this structure if you have a better architectural approach.

9. Testing Requirements

Use Jest and React Testing Library.

Write tests covering:

* Modal open and close.
* Escape key behavior.
* Overlay click behavior.
* Focus trapping.
* Focus restoration.
* Dynamic footer with 1, 2, 3, or more buttons.
* Modal without header.
* Modal without footer.
* Accessibility attributes.
* React Strict Mode behavior.
* Multiple modal instances.
* Body scroll cleanup.
* Responsive behavior where applicable.

Include accessibility testing recommendations using axe-core.

10. Expected Deliverables

Provide:

1. Complete architecture explanation.
2. Complete implementation of every file.
3. Fully typed TypeScript interfaces.
4. Complete CSS.
5. Usage examples.
6. Examples with dynamic footer buttons.
7. Examples with forms and submit actions.
8. Jest + React Testing Library test cases.
9. Accessibility explanation.
10. Edge cases and production considerations.

11. Important Instructions

* Do not provide pseudocode.
* Do not skip implementation files.
* Do not leave TODO comments instead of actual implementations.
* Do not use third-party modal libraries.
* Ensure all imports and exports are correct.
* Ensure the code is consistent across all files.
* Explain important architectural decisions.
* Highlight any limitations or browser compatibility considerations.
* Prioritize accessibility, maintainability, performance, and production readiness.

Before writing the implementation, briefly explain the proposed architecture and identify any important design decisions. Then provide the complete working implementation.

Final Goal: Build a reusable, enterprise-grade Modal component suitable for a professional React + TypeScript component library or design system.