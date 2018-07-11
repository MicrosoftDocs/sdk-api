---
UID: NN:tom.ITextDocument2
title: ITextDocument2
author: windows-sdk-content
description: Extends the ITextDocument interface, adding methods that enable the Input Method Editor (IME) to drive the rich edit control, and methods to retrieve other interfaces such as ITextDisplays, ITextRange2, ITextFont2, ITextPara2, and so on.
old-location: controls\itextdocument2.htm
old-project: controls
ms.assetid: 0b0a54d7-7606-41f6-b8be-6367d9180ef4
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ITextDocument2, ITextDocument2 interface [Windows Controls], ITextDocument2 interface [Windows Controls],described, controls.itextdocument2, tom/ITextDocument2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextDocument2
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/library/Bb774052(v=VS.85).aspx">ITextDocument</a> interface, adding methods that enable the Input Method Editor (IME) to drive the rich edit control, and methods to retrieve other interfaces such as  <a href="https://msdn.microsoft.com/e7266734-c066-4f80-8d3d-99ffb251cd39">ITextDisplays</a>, <a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>, <a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>, <a href="https://msdn.microsoft.com/31a0849f-c651-4178-b1ff-a4333bcde5d9">ITextPara2</a>, and so on. 

Some <b>ITextDocument2</b> methods used with the IME need access to the current window handle (<b>HWND</b>). Use the <a href="https://msdn.microsoft.com/4bf5e644-292e-4847-8dad-71e8ccf86205">ITextDocument2::GetWindow</a> method to retrieve the handle.


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
<a href="https://msdn.microsoft.com/055b9d59-59cc-4922-b6b9-920885969dbc">AttachMsgFilter</a>
</td>
<td align="left" width="63%">
Attaches a new message filter to the edit instance. All window messages that the edit instance receives are forwarded to the message filter. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c3aae14-8fa4-47bf-93ae-1d34333f0356">CheckTextLimit</a>
</td>
<td align="left" width="63%">
Checks whether the number of characters to be added would exceed the maximum text limit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9849d958-5bcf-44d9-827c-3d5619ba2357">GetActiveStory</a>
</td>
<td align="left" width="63%">
Gets the active story; that is, the story that receives keyboard and mouse input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a90e6f5-1231-45fc-868f-4f24ed195638">GetCallManager</a>
</td>
<td align="left" width="63%">
Gets the call manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ab170d2-50a3-4fbf-8e02-92b031bc1e4f">GetCaretType</a>
</td>
<td align="left" width="63%">
Gets the caret type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5736c58-e402-421d-aa4a-79b65460b692">GetClientRect</a>
</td>
<td align="left" width="63%">
Retrieves the client rectangle of the rich edit control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f610b45-9c17-4b20-82e0-fa78169360cc">GetDisplays</a>
</td>
<td align="left" width="63%">
Gets the displays collection for this TOM engine instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b028c2f6-8c8e-49f8-bf53-f4a639cb16c2">GetDocumentFont</a>
</td>
<td align="left" width="63%">
Gets an object that provides the default character format information for this instance of the TOM engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3667587e-3cf1-4b86-82fd-2fc34d4cbeee">GetDocumentPara</a>
</td>
<td align="left" width="63%">
Gets an object that provides the default paragraph format  information for this instance of the TOM engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/730c869d-cac0-40ce-b6c5-ca3be2c94419">GetEastAsianFlags</a>
</td>
<td align="left" width="63%">
Gets the East Asian flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bc2740e-852f-430b-913e-5d28baec3272">GetEffectColor</a>
</td>
<td align="left" width="63%">
Retrieves the color used for special text attributes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22cfa44e-3603-458b-991e-6e536df63803">GetGenerator</a>
</td>
<td align="left" width="63%">
Gets the name of the TOM engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42ee6d71-b51d-459a-b1af-638a19d8be2c">GetImmContext</a>
</td>
<td align="left" width="63%">
Gets the IMM input context from the TOM host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/732165f2-e6cd-4f39-85c6-06faebfa65e2">GetMainStory</a>
</td>
<td align="left" width="63%">
Gets the main story.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7686d0d6-5f49-4ab6-8a9e-1e53447ffe27">GetMathProperties</a>
</td>
<td align="left" width="63%">
Gets the math properties for the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d6ef859-150b-41e7-be58-b9c87c61f7d8">GetNewStory</a>
</td>
<td align="left" width="63%">
Gets a new story.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/720f9759-96c1-45f0-9251-90d60532d247">GetNotificationMode</a>
</td>
<td align="left" width="63%">
Gets the notification mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d07c3093-8050-4c62-8e90-3b09cdb10700">GetPreferredFont</a>
</td>
<td align="left" width="63%">
Retrieves the preferred font for a particular character repertoire and character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30775a51-0e63-453e-ac94-39d4510002f0">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves the value of a property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a81fde9e-aef8-49cf-88b2-d0416195d70a">GetSelection2</a>
</td>
<td align="left" width="63%">
Gets the active selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb1322e9-47b2-4770-b5de-c5eeda70eed1">GetStory</a>
</td>
<td align="left" width="63%">
Retrieves the story that corresponds to a particular index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec62db67-d5e6-47d9-ad35-0fc33ba45b6b">GetStoryRanges2</a>
</td>
<td align="left" width="63%">
Gets an object for enumerating the stories in a document. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54d8c682-4e30-4ce2-baa1-d89e28491015">GetStrings</a>
</td>
<td align="left" width="63%">
Gets a collection of rich-text strings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3433954c-818b-4811-9e38-4bc8ab3ee7f9">GetTypographyOptions</a>
</td>
<td align="left" width="63%">
Gets the typography options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4cc4502b-4e7c-4561-b7d4-a248bf248a8a">GetVersion</a>
</td>
<td align="left" width="63%">
Gets the version number of the TOM engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bf5e644-292e-4847-8dad-71e8ccf86205">GetWindow</a>
</td>
<td align="left" width="63%">
Gets the handle of the window that the TOM engine is using to display output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c7962a5-5f8d-4db1-bb94-a77738cf75bb">Notify</a>
</td>
<td align="left" width="63%">
Notifies the TOM engine client of particular IME events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0cd3788-de0e-4b57-8f24-f0897e2b0bed">Range2</a>
</td>
<td align="left" width="63%">
Retrieves a new text range for the active story of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3212c6cc-a1fb-44ca-aba9-2234414e7a39">RangeFromPoint2</a>
</td>
<td align="left" width="63%">
Retrieves the degenerate range at (or nearest to) a particular point on the screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d17fdcb-502c-43ab-9f74-7247a1f14f45">ReleaseCallManager</a>
</td>
<td align="left" width="63%">
Releases the call manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2172e20b-2343-4a65-a08e-0d8b8c101860">ReleaseImmContext</a>
</td>
<td align="left" width="63%">
Releases an IMM input context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c71673c-5119-4906-99e0-1a2aa04589e1">SetActiveStory</a>
</td>
<td align="left" width="63%">
Sets the active story; that is, the story that receives keyboard and mouse input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40d34482-cf07-4401-ad02-f5d1b0184976">SetCaretType</a>
</td>
<td align="left" width="63%">
Sets the caret type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fbc000a-76c2-4b80-856b-42f2e1829e93">SetDocumentFont</a>
</td>
<td align="left" width="63%">
Sets  the default character formatting for this instance of the TOM engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d35d57e9-a005-48cd-a92d-381dc490d44f">SetDocumentPara</a>
</td>
<td align="left" width="63%">
Sets the default paragraph formatting  for this instance of the TOM engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6371b525-96da-42a7-8cee-228b47208f46">SetEffectColor</a>
</td>
<td align="left" width="63%">
Specifies the color to use for special text attributes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65db4e97-48c9-48e0-b436-2b2e6713bebd">SetIMEInProgress</a>
</td>
<td align="left" width="63%">
Sets the state of the IME in-progress flag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a688354b-b231-44fc-9cfb-32c8e8b1361f">SetMathProperties</a>
</td>
<td align="left" width="63%">
Specifies the math properties to use for the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3dd9895-9fdd-4919-9e3a-382bb130f4b9">SetNotificationMode</a>
</td>
<td align="left" width="63%">
Sets the notification mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29e70a21-9fab-4fba-9cc4-f1268b005edb">SetProperty</a>
</td>
<td align="left" width="63%">
Specifies a new value for a property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1013c9bf-b6fe-4396-b7a8-36e61edf1df3">SetTypographyOptions</a>
</td>
<td align="left" width="63%">
Specifies the typography options for the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f1f83a0-9308-40c8-b889-aa8118ee9e71">SysBeep</a>
</td>
<td align="left" width="63%">
Generates a system beep.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927294">Update</a>
</td>
<td align="left" width="63%">
Updates the selection and caret.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85bb0a41-e3a7-43ab-bc14-fdd4dae2ee69">UpdateWindow</a>
</td>
<td align="left" width="63%">
Notifies the client that the view has changed and the client should update the view if the TOM engine is in-place active.

</td>
</tr>
</table> 

