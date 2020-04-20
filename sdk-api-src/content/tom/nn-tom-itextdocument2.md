---
UID: NN:tom.ITextDocument2
title: ITextDocument2 (tom.h)
description: Extends the ITextDocument interface, adding methods that enable the Input Method Editor (IME) to drive the rich edit control, and methods to retrieve other interfaces such as ITextDisplays, ITextRange2, ITextFont2, ITextPara2, and so on.helpviewer_keywords: ["ITextDocument2","ITextDocument2 interface [Windows Controls]","ITextDocument2 interface [Windows Controls]","described","controls.itextdocument2","tom/ITextDocument2"]
old-location: controls\itextdocument2.htm
tech.root: Controls
ms.assetid: 0b0a54d7-7606-41f6-b8be-6367d9180ef4
ms.date: 12/05/2018
ms.keywords: ITextDocument2, ITextDocument2 interface [Windows Controls], ITextDocument2 interface [Windows Controls],described, controls.itextdocument2, tom/ITextDocument2
f1_keywords:
- tom/ITextDocument2
dev_langs:
- c++
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- ITextDocument2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextDocument2 interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a> interface, adding methods that enable the Input Method Editor (IME) to drive the rich edit control, and methods to retrieve other interfaces such as  <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextdisplays">ITextDisplays</a>, <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>, <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>, <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a>, and so on. 

Some <b>ITextDocument2</b> methods used with the IME need access to the current window handle (<b>HWND</b>). Use the <a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getwindow">ITextDocument2::GetWindow</a> method to retrieve the handle.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextDocument2</b> interface inherits from <b>ITextDocument</b>. <b>ITextDocument2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextDocument2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-attachmsgfilter">AttachMsgFilter</a>
</td>
<td align="left" width="63%">
Attaches a new message filter to the edit instance. All window messages that the edit instance receives are forwarded to the message filter. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-checktextlimit">CheckTextLimit</a>
</td>
<td align="left" width="63%">
Checks whether the number of characters to be added would exceed the maximum text limit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getactivestory">GetActiveStory</a>
</td>
<td align="left" width="63%">
Gets the active story; that is, the story that receives keyboard and mouse input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getcallmanager">GetCallManager</a>
</td>
<td align="left" width="63%">
Gets the call manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getcarettype">GetCaretType</a>
</td>
<td align="left" width="63%">
Gets the caret type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getclientrect">GetClientRect</a>
</td>
<td align="left" width="63%">
Retrieves the client rectangle of the rich edit control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getdisplays">GetDisplays</a>
</td>
<td align="left" width="63%">
Gets the displays collection for this TOM engine instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getdocumentfont">GetDocumentFont</a>
</td>
<td align="left" width="63%">
Gets an object that provides the default character format information for this instance of the TOM engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getdocumentpara">GetDocumentPara</a>
</td>
<td align="left" width="63%">
Gets an object that provides the default paragraph format  information for this instance of the TOM engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-geteastasianflags">GetEastAsianFlags</a>
</td>
<td align="left" width="63%">
Gets the East Asian flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-geteffectcolor">GetEffectColor</a>
</td>
<td align="left" width="63%">
Retrieves the color used for special text attributes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getgenerator">GetGenerator</a>
</td>
<td align="left" width="63%">
Gets the name of the TOM engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getimmcontext">GetImmContext</a>
</td>
<td align="left" width="63%">
Gets the IMM input context from the TOM host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getmainstory">GetMainStory</a>
</td>
<td align="left" width="63%">
Gets the main story.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getmathproperties">GetMathProperties</a>
</td>
<td align="left" width="63%">
Gets the math properties for the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getnewstory">GetNewStory</a>
</td>
<td align="left" width="63%">
Gets a new story.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getnotificationmode">GetNotificationMode</a>
</td>
<td align="left" width="63%">
Gets the notification mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getpreferredfont">GetPreferredFont</a>
</td>
<td align="left" width="63%">
Retrieves the preferred font for a particular character repertoire and character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves the value of a property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getselection2">GetSelection2</a>
</td>
<td align="left" width="63%">
Gets the active selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getstory">GetStory</a>
</td>
<td align="left" width="63%">
Retrieves the story that corresponds to a particular index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getstoryranges2">GetStoryRanges2</a>
</td>
<td align="left" width="63%">
Gets an object for enumerating the stories in a document. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getstrings">GetStrings</a>
</td>
<td align="left" width="63%">
Gets a collection of rich-text strings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-gettypographyoptions">GetTypographyOptions</a>
</td>
<td align="left" width="63%">
Gets the typography options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getversion">GetVersion</a>
</td>
<td align="left" width="63%">
Gets the version number of the TOM engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getwindow">GetWindow</a>
</td>
<td align="left" width="63%">
Gets the handle of the window that the TOM engine is using to display output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-notify">Notify</a>
</td>
<td align="left" width="63%">
Notifies the TOM engine client of particular IME events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-range2">Range2</a>
</td>
<td align="left" width="63%">
Retrieves a new text range for the active story of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-rangefrompoint2">RangeFromPoint2</a>
</td>
<td align="left" width="63%">
Retrieves the degenerate range at (or nearest to) a particular point on the screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-releasecallmanager">ReleaseCallManager</a>
</td>
<td align="left" width="63%">
Releases the call manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-releaseimmcontext">ReleaseImmContext</a>
</td>
<td align="left" width="63%">
Releases an IMM input context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-setactivestory">SetActiveStory</a>
</td>
<td align="left" width="63%">
Sets the active story; that is, the story that receives keyboard and mouse input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-setcarettype">SetCaretType</a>
</td>
<td align="left" width="63%">
Sets the caret type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-setdocumentfont">SetDocumentFont</a>
</td>
<td align="left" width="63%">
Sets  the default character formatting for this instance of the TOM engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-setdocumentpara">SetDocumentPara</a>
</td>
<td align="left" width="63%">
Sets the default paragraph formatting  for this instance of the TOM engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-seteffectcolor">SetEffectColor</a>
</td>
<td align="left" width="63%">
Specifies the color to use for special text attributes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-setimeinprogress">SetIMEInProgress</a>
</td>
<td align="left" width="63%">
Sets the state of the IME in-progress flag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-setmathproperties">SetMathProperties</a>
</td>
<td align="left" width="63%">
Specifies the math properties to use for the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-setnotificationmode">SetNotificationMode</a>
</td>
<td align="left" width="63%">
Sets the notification mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Specifies a new value for a property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-settypographyoptions">SetTypographyOptions</a>
</td>
<td align="left" width="63%">
Specifies the typography options for the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-sysbeep">SysBeep</a>
</td>
<td align="left" width="63%">
Generates a system beep.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-update">Update</a>
</td>
<td align="left" width="63%">
Updates the selection and caret.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-updatewindow">UpdateWindow</a>
</td>
<td align="left" width="63%">
Notifies the client that the view has changed and the client should update the view if the TOM engine is in-place active.

</td>
</tr>
</table> 

