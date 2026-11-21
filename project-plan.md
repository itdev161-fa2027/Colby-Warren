# Final Project Plan

## Milestone 1: Plan

Path: B

### Enhancement: Markdown Support

What the user will see: Users will be able to format their blog posts using Markdown, including headings, bold text, lists, links, and code blocks. A preview will allow users to see how their posts will look before saving them. Published posts will display the formatting correctly.

Back-end changes: None. Markdown content will be stored as plain text in the existing Post model's body field.

Front-end changes: Update PostDetail.jsx to render Markdown using react-markdown and remark-gfm. Update PostForm.jsx to include a Markdown preview. Update PostCard.jsx to display readable previews without unnecessary Markdown symbols. Add CSS styling for headings, lists, links, and code blocks.

New packages: react-markdown, remark-gfm, and remove-markdown.

What I will test:

- Headings, bold text, italic text, and links display correctly.
- Ordered and unordered lists display correctly.
- Code blocks display using a monospace font.
- The Markdown preview matches the published post.
- HTML entered into a post does not execute as code.
- Post cards display readable previews without Markdown symbols.

### Enhancement: Post Categories

What the user will see: Users will be able to select a category when creating or editing a blog post. Categories such as Technology, Lifestyle, and Tutorial will appear on posts. Visitors will be able to filter posts by category on the home page.

Back-end changes: Add a category field to the Post schema using a fixed list of valid categories. Update the POST and PUT routes in server.js to validate categories. Update GET /api/posts to accept a category query parameter and return matching posts. Ensure posts created before the enhancement remain visible.

Front-end changes: Add a category dropdown to PostForm.jsx. Display categories in PostCard.jsx and PostDetail.jsx. Add a category filter to Home.jsx and keep it visible while posts load. Update getPosts in client/src/services/api.js to send the selected category.

New packages: None

What I will test:

- Users can select a valid category when creating a post.
- Users can change a post's category when editing.
- Categories display correctly on post cards and post details.
- Selecting a category filter displays only matching posts.
- Selecting All displays every post.
- The server rejects invalid or missing categories on new posts.
- Posts created before categories were added remain visible.

### Task List

1. Review the existing blog application and confirm Activity 9 features work - Project Week 1
2. Create the project plan and select enhancements - Project Week 1
3. Install Markdown packages and update PostDetail.jsx - Project Week 2
4. Add Markdown preview to PostForm.jsx - Project Week 2
5. Update PostCard.jsx and add Markdown styling - Project Week 2
6. Add the category field to the Post model - Project Week 2
7. Update server.js to validate and filter post categories - Project Week 2
8. Add the category dropdown to PostForm.jsx - Project Week 3
9. Display categories in PostCard.jsx and PostDetail.jsx - Project Week 3
10. Add category filtering to Home.jsx and update api.js - Project Week 3
11. Test both enhancements and existing authentication and CRUD features - Project Week 3
12. Update the project plan for Milestone 2 and record progress - Project Week 3
13. Complete final testing and fix remaining issues - Project Week 4
14. Update README.md with features, dependencies, and setup instructions - Project Week 4
15. Record the final project demonstration video - Project Week 4
16. Complete final documentation, commit changes, and prepare the GitHub submission - Project Week 4

### Questions or Risks

One concern is making sure Markdown formatting displays correctly without allowing unsafe HTML to execute. I will follow the react-markdown documentation and test posts containing HTML.

Another concern is adding categories without breaking posts created during earlier activities. I will test older posts and determine how to display posts that do not have a category.

I will also test the existing registration, login, and post CRUD features after making changes to ensure they continue working.

## AI Usage

Tools: Copilot

What I used them for:

- Reviewing the final project instructions and comparing enhancement options.
- Choosing two compatible Medium enhancements for Path B.
- Organizing the project plan, development tasks, and testing checklist.

How I checked the result: I compared the plan with the professor's Final Project instructions and Enhancement Options document. I will verify the implementation through browser testing and review the code before submitting the completed project.
