---
UID: NN:photoacquire.IUserInputString
title: IUserInputString (photoacquire.h)
author: windows-sdk-content
description: The IUserInputString interface represents the object created when asking the user for a string&#8212;for example, when obtaining the name of a tag.
old-location: picacq\iuserinputstring.htm
tech.root: acquisition
ms.assetid: f942fefc-2db1-4067-8311-f9ebbaca9d31
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUserInputString, IUserInputString interface [Picture Acquisition], IUserInputString interface [Picture Acquisition],described, IUserInputStringInterface, photoacquire/IUserInputString, picacq.iuserinputstring
ms.topic: interface
f1_keywords: ["photoacquire/IUserInputString"]
req.header: photoacquire.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - photoacquire.h
api_name:
 - IUserInputString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUserInputString interface


## -description



The <b>IUserInputString</b> interface represents the object created when asking the user for a string—for example, when obtaining the name of a tag.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUserInputString</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUserInputString</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUserInputString</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iuserinputstring-getdefault">GetDefault</a>
</td>
<td align="left" width="63%">
Retrieves the default string used to initialize an edit control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iuserinputstring-getimage">GetImage</a>
</td>
<td align="left" width="63%">
Retrieves the default image used to initialize an edit control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iuserinputstring-getmaxlength">GetMaxLength</a>
</td>
<td align="left" width="63%">
Retrieves the maximum string length the user interface (UI) should allow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iuserinputstring-getmrucount">GetMruCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the list of most recently used items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iuserinputstring-getmruentryat">GetMruEntryAt</a>
</td>
<td align="left" width="63%">
Retrieves the entry at the given index in the most recently used list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iuserinputstring-getprompt">GetPrompt</a>
</td>
<td align="left" width="63%">
Retrieves the title of a prompt if the prompt is a modal dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iuserinputstring-getstringid">GetStringId</a>
</td>
<td align="left" width="63%">
Retrieves the unlocalized canonical name for the requested string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iuserinputstring-getstringtype">GetStringType</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the type of string to obtain from the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iuserinputstring-getsubmitbuttontext">GetSubmitButtonText</a>
</td>
<td align="left" width="63%">
Retrieves the text for the submit button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iuserinputstring-gettooltiptext">GetTooltipText</a>
</td>
<td align="left" width="63%">
Retrieves the tooltip text displayed for a control.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/acquisition/interfaces">Interfaces</a>
 

 

