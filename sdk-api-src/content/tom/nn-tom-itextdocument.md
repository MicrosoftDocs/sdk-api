---
UID: NN:tom.ITextDocument
title: ITextDocument (tom.h)
author: windows-sdk-content
description: The ITextDocument interface is the Text Object Model (TOM) top-level interface, which retrieves the active selection and range objects for any story in the document&#8212;whether active or not.
old-location: controls\ITextDocument.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextdocument.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextDocument, ITextDocument interface [Windows Controls], ITextDocument interface [Windows Controls],described, _win32_ITextDocument, _win32_ITextDocument_cpp, controls.ITextDocument, controls._win32_ITextDocument, tom/ITextDocument
ms.topic: interface
f1_keywords: 
 - "tom/ITextDocument"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextDocument interface


## -description


The <b>ITextDocument</b> interface is the Text Object Model (TOM) top-level interface, which retrieves the active selection and range objects for any story in the document—whether active or not. It enables the application to: 
        
<ul>
<li>Open and save documents.</li>
<li>Control undo behavior and screen updating.</li>
<li>Find a range from a screen position.</li>
<li>Get an <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextstoryranges">ITextStoryRanges</a> story enumerator.</li>
</ul><b>When to Implement</b>

Applications typically do not implement the <b>ITextDocument</b> interface. Microsoft text solutions, such as rich edit controls, implement <b>ITextDocument</b> as part of their TOM implementation. 

<b>When to Use</b>

Applications can retrieve an <b>ITextDocument</b> pointer from a rich edit control. To do this, send an <a href="https://docs.microsoft.com/windows/desktop/Controls/em-getoleinterface">EM_GETOLEINTERFACE</a> message to retrieve an <a href="https://docs.microsoft.com/windows/desktop/api/richole/nn-richole-iricheditole">IRichEditOle</a> object from a rich edit control. Then, call the object's <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IUnknown::QueryInterface</a> method to retrieve an <b>ITextDocument</b> pointer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextDocument</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextDocument</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-begineditcollection">BeginEditCollection</a>
</td>
<td align="left" width="63%">
Turns on edit collection (also called <i>undo grouping</i>). 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-endeditcollection">EndEditCollection</a>
</td>
<td align="left" width="63%">
Turns off edit collection (also called <i>undo grouping</i>). 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-freeze">Freeze</a>
</td>
<td align="left" width="63%">
Increments the freeze count. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-getdefaulttabstop">GetDefaultTabStop</a>
</td>
<td align="left" width="63%">
Gets the default tab width.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-getname">GetName</a>
</td>
<td align="left" width="63%">
Gets the file name of this document. This is the <b>ITextDocument</b> default property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-getsaved">GetSaved</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether changes have been made since the file was last saved. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-getselection">GetSelection</a>
</td>
<td align="left" width="63%">
Gets the active selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-getstorycount">GetStoryCount</a>
</td>
<td align="left" width="63%">
Gets the count of stories in this document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-getstoryranges">GetStoryRanges</a>
</td>
<td align="left" width="63%">
Gets the story collection object used to enumerate the stories in a document. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-new">New</a>
</td>
<td align="left" width="63%">
Opens a new document. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-open">Open</a>
</td>
<td align="left" width="63%">
Opens a specified document. There are parameters to specify access and sharing privileges, creation and conversion of the file, as well as the code page for the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-range">Range</a>
</td>
<td align="left" width="63%">
Retrieves a text range object for a specified range of content in the active story of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-rangefrompoint">RangeFromPoint</a>
</td>
<td align="left" width="63%">
Retrieves a range for the content at or nearest to the specified point on the screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-redo">Redo</a>
</td>
<td align="left" width="63%">
Performs a specified number of redo operations. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-save">Save</a>
</td>
<td align="left" width="63%">
Saves the document. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-setdefaulttabstop">SetDefaultTabStop</a>
</td>
<td align="left" width="63%">
Sets the default tab stop, which is used when no tab exists beyond the current display position. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-setsaved">SetSaved</a>
</td>
<td align="left" width="63%">
Sets the document 
			<b>Saved</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-undo">Undo</a>
</td>
<td align="left" width="63%">
Performs a specified number of undo operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-unfreeze">Unfreeze</a>
</td>
<td align="left" width="63%">
Decrements the freeze count. 

</td>
</tr>
</table> 


## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/Controls/text-object-model">Text Object Model</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/using-the-text-object-model">Using The Text Object Model</a>
 

 

