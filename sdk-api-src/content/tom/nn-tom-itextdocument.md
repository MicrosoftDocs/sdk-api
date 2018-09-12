---
UID: NN:tom.ITextDocument
title: ITextDocument
author: windows-sdk-content
description: The ITextDocument interface is the Text Object Model (TOM) top-level interface, which retrieves the active selection and range objects for any story in the document&#8212;whether active or not.
old-location: controls\ITextDocument.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextdocument.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
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
<li>Get an <a href="https://msdn.microsoft.com/en-us/library/Bb774062(v=VS.85).aspx">ITextStoryRanges</a> story enumerator.</li>
</ul><b>When to Implement</b>

Applications typically do not implement the <b>ITextDocument</b> interface. Microsoft text solutions, such as rich edit controls, implement <b>ITextDocument</b> as part of their TOM implementation. 

<b>When to Use</b>

Applications can retrieve an <b>ITextDocument</b> pointer from a rich edit control. To do this, send an <a href="https://msdn.microsoft.com/en-us/library/Bb788041(v=VS.85).aspx">EM_GETOLEINTERFACE</a> message to retrieve an <a href="https://msdn.microsoft.com/en-us/library/Bb774306(v=VS.85).aspx">IRichEditOle</a> object from a rich edit control. Then, call the object's <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> method to retrieve an <b>ITextDocument</b> pointer.


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
<a href="https://msdn.microsoft.com/en-us/library/Bb787730(v=VS.85).aspx">BeginEditCollection</a>
</td>
<td align="left" width="63%">
Turns on edit collection (also called <i>undo grouping</i>). 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787750(v=VS.85).aspx">EndEditCollection</a>
</td>
<td align="left" width="63%">
Turns off edit collection (also called <i>undo grouping</i>). 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773925(v=VS.85).aspx">Freeze</a>
</td>
<td align="left" width="63%">
Increments the freeze count. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773941(v=VS.85).aspx">GetDefaultTabStop</a>
</td>
<td align="left" width="63%">
Gets the default tab width.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787871(v=VS.85).aspx">GetName</a>
</td>
<td align="left" width="63%">
Gets the file name of this document. This is the <b>ITextDocument</b> default property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774011(v=VS.85).aspx">GetSaved</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether changes have been made since the file was last saved. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774013(v=VS.85).aspx">GetSelection</a>
</td>
<td align="left" width="63%">
Gets the active selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774027(v=VS.85).aspx">GetStoryCount</a>
</td>
<td align="left" width="63%">
Gets the count of stories in this document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774029(v=VS.85).aspx">GetStoryRanges</a>
</td>
<td align="left" width="63%">
Gets the story collection object used to enumerate the stories in a document. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774091(v=VS.85).aspx">New</a>
</td>
<td align="left" width="63%">
Opens a new document. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774093(v=VS.85).aspx">Open</a>
</td>
<td align="left" width="63%">
Opens a specified document. There are parameters to specify access and sharing privileges, creation and conversion of the file, as well as the code page for the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774097(v=VS.85).aspx">Range</a>
</td>
<td align="left" width="63%">
Retrieves a text range object for a specified range of content in the active story of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774099(v=VS.85).aspx">RangeFromPoint</a>
</td>
<td align="left" width="63%">
Retrieves a range for the content at or nearest to the specified point on the screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774101(v=VS.85).aspx">Redo</a>
</td>
<td align="left" width="63%">
Performs a specified number of redo operations. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774103(v=VS.85).aspx">Save</a>
</td>
<td align="left" width="63%">
Saves the document. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774135(v=VS.85).aspx">SetDefaultTabStop</a>
</td>
<td align="left" width="63%">
Sets the default tab stop, which is used when no tab exists beyond the current display position. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787809(v=VS.85).aspx">SetSaved</a>
</td>
<td align="left" width="63%">
Sets the document 
			<b>Saved</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787837(v=VS.85).aspx">Undo</a>
</td>
<td align="left" width="63%">
Performs a specified number of undo operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787838(v=VS.85).aspx">Unfreeze</a>
</td>
<td align="left" width="63%">
Decrements the freeze count. 

</td>
</tr>
</table> 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787726(v=VS.85).aspx">Using The Text Object Model</a>
 

 

