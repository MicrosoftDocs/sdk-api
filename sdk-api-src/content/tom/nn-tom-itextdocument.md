---
UID: NN:tom.ITextDocument
title: ITextDocument
author: windows-sdk-content
description: The ITextDocument interface is the Text Object Model (TOM) top-level interface, which retrieves the active selection and range objects for any story in the document&#8212;whether active or not.
old-location: controls\ITextDocument.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextdocument.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ITextDocument, ITextDocument interface [Windows Controls], ITextDocument interface [Windows Controls],described, _win32_ITextDocument, _win32_ITextDocument_cpp, controls.ITextDocument, controls._win32_ITextDocument, tom/ITextDocument
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextDocument
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument interface


## -description


The <b>ITextDocument</b> interface is the Text Object Model (TOM) top-level interface, which retrieves the active selection and range objects for any story in the document—whether active or not. It enables the application to: 
        
<ul>
<li>Open and save documents.</li>
<li>Control undo behavior and screen updating.</li>
<li>Find a range from a screen position.</li>
<li>Get an <a href="https://msdn.microsoft.com/eee6c992-1f6a-4e4e-bd8a-34a9aff41859">ITextStoryRanges</a> story enumerator.</li>
</ul><b>When to Implement</b>

Applications typically do not implement the <b>ITextDocument</b> interface. Microsoft text solutions, such as rich edit controls, implement <b>ITextDocument</b> as part of their TOM implementation. 

<b>When to Use</b>

Applications can retrieve an <b>ITextDocument</b> pointer from a rich edit control. To do this, send an <a href="https://msdn.microsoft.com/fa462c7b-29b9-4694-b7ad-6068c69ffb76">EM_GETOLEINTERFACE</a> message to retrieve an <a href="https://msdn.microsoft.com/d6d1794b-f16c-4a8c-84f5-dfe8bd8be08c">IRichEditOle</a> object from a rich edit control. Then, call the object's <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> method to retrieve an <b>ITextDocument</b> pointer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextDocument</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITextDocument</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextDocument</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/145cdaa0-b800-47da-a964-712e80287a3b">BeginEditCollection</a>
</td>
<td align="left" width="63%">
Turns on edit collection (also called <i>undo grouping</i>). 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92cd216c-b048-4157-906b-3ef4418d2613">EndEditCollection</a>
</td>
<td align="left" width="63%">
Turns off edit collection (also called <i>undo grouping</i>). 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39ddce52-589e-4dc4-a55c-48902c2fa51e">Freeze</a>
</td>
<td align="left" width="63%">
Increments the freeze count. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7005c4d-3280-4c06-9b23-74e6742f4970">GetDefaultTabStop</a>
</td>
<td align="left" width="63%">
Gets the default tab width.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49483973-6880-4a40-92e5-38de02523e6d">GetName</a>
</td>
<td align="left" width="63%">
Gets the file name of this document. This is the <b>ITextDocument</b> default property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50f38968-c647-49cc-b8b9-7c5329891ab9">GetSaved</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether changes have been made since the file was last saved. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c62c4a0-b5fe-406d-b175-693032dbe94a">GetSelection</a>
</td>
<td align="left" width="63%">
Gets the active selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a9d865c-8710-4e67-bf1a-10d09f81488c">GetStoryCount</a>
</td>
<td align="left" width="63%">
Gets the count of stories in this document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e542bd10-228a-4d9a-bd62-c721e56c6369">GetStoryRanges</a>
</td>
<td align="left" width="63%">
Gets the story collection object used to enumerate the stories in a document. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69f90d70-dac6-4f20-91e5-858fe9253c50">New</a>
</td>
<td align="left" width="63%">
Opens a new document. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ea20837-4987-49c9-88e5-81d79c9016ac">Open</a>
</td>
<td align="left" width="63%">
Opens a specified document. There are parameters to specify access and sharing privileges, creation and conversion of the file, as well as the code page for the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0a14c38-4c07-47d6-b854-f56a0c7ef2e7">Range</a>
</td>
<td align="left" width="63%">
Retrieves a text range object for a specified range of content in the active story of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9380e07f-ff09-480c-8ce8-6752fcbd0bb8">RangeFromPoint</a>
</td>
<td align="left" width="63%">
Retrieves a range for the content at or nearest to the specified point on the screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45d8c366-a50a-4a0f-96c8-aa31629e280f">Redo</a>
</td>
<td align="left" width="63%">
Performs a specified number of redo operations. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd81fcee-c792-4f7a-b5ee-cd63deafb08a">Save</a>
</td>
<td align="left" width="63%">
Saves the document. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/229d5df7-6d1e-4be1-b5f9-7ccfdf2b0bfb">SetDefaultTabStop</a>
</td>
<td align="left" width="63%">
Sets the default tab stop, which is used when no tab exists beyond the current display position. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a0a7196-de8d-4550-b945-d1b0ebb644ef">SetSaved</a>
</td>
<td align="left" width="63%">
Sets the document 
			<b>Saved</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27faab46-e836-4090-98aa-a6cd3e5ecd22">Undo</a>
</td>
<td align="left" width="63%">
Performs a specified number of undo operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b17e081-1d1f-460c-8176-8da1bd4ee9f1">Unfreeze</a>
</td>
<td align="left" width="63%">
Decrements the freeze count. 

</td>
</tr>
</table> 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>



<a href="https://msdn.microsoft.com/5d9ab4fa-e9a0-4031-bbaa-311aff912eba">Using The Text Object Model</a>
 

 

