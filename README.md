# NorwayTemplate V2.3

1，修复了设置time limitation 时的bug

2，添加了四个新的function，t:getDateOfBlogPostIdChange(), t:getNumberOfBlogPostIdChange(), t:getDateOfCommentIdChange() and t:getNumberOfCommentIdChange() 它们用于生成使用新规则的blog uri和comment uri。

3，修复了forums中处理replies的bug

这次的更新中，最重要的是第二条，我们对blog id和comment id制定了新的规则。

首先，以blog id为例，在我们的老模板中，id部分是直接使用t:getBlogPostId，在新模板中，以新规则生成的id，将包含三个部分，t:getDateOfBlogPostIdChange_t:getNumberOfBlogPostIdChange_t:getBlogPostId。其中t:getDateOfBlogPostIdChange_t:getNumberOfBlogPostIdChange部分的作用是，它被用来作为blog id的版本编号。当且仅当t:getBlogPostId改变时，t:getDateOfBlogPostIdChange_t:getNumberOfBlogPostIdChange也应该跟着变化。t:getDateOfBlogPostIdChange_t:getNumberOfBlogPostIdChange的变化规则，请参照模板中的描述。

comment id同理。
