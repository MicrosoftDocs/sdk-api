---
UID: NN:photoacquire.IUserInputString
title: IUserInputString
author: windows-sdk-content
description: The IUserInputString interface represents the object created when asking the user for a string&#8212;for example, when obtaining the name of a tag.
old-location: picacq\iuserinputstring.htm
tech.root: acquisition
ms.assetid: f942fefc-2db1-4067-8311-f9ebbaca9d31
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IUserInputString, IUserInputString interface [Picture Acquisition], IUserInputString interface [Picture Acquisition],described, IUserInputStringInterface, photoacquire/IUserInputString, picacq.iuserinputstring
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
---

# IUserInputString interface


## -description



The <b>IUserInputString</b> interface represents the object created when asking the user for a string—for example, when obtaining the name of a tag.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUserInputString</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUserInputString</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d9e967f9-47ed-4b55-a728-fe6432b44efd">GetDefault</a>
</td>
<td align="left" width="63%">
Retrieves the default string used to initialize an edit control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a626c53d-b9dd-483b-924d-6f5d2d1c2663">GetImage</a>
</td>
<td align="left" width="63%">
Retrieves the default image used to initialize an edit control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/474b32f5-e8b3-49d2-a2de-a78244b9066e">GetMaxLength</a>
</td>
<td align="left" width="63%">
Retrieves the maximum string length the user interface (UI) should allow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47f1a916-2d1e-4fe8-837b-3e9bf4e51c0b">GetMruCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the list of most recently used items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d03c3eba-e55c-421d-acfa-fea6aa645cc5">GetMruEntryAt</a>
</td>
<td align="left" width="63%">
Retrieves the entry at the given index in the most recently used list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2fdb18d-5af8-45c8-8f92-7fc8c836082d">GetPrompt</a>
</td>
<td align="left" width="63%">
Retrieves the title of a prompt if the prompt is a modal dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29c4b592-fa6a-4f9b-a390-e8bc0928a26d">GetStringId</a>
</td>
<td align="left" width="63%">
Retrieves the unlocalized canonical name for the requested string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57f0c750-9c66-4c30-adc1-0cfd23d878d1">GetStringType</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the type of string to obtain from the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00cb081a-9077-4ecc-9a1f-002072e6ddda">GetSubmitButtonText</a>
</td>
<td align="left" width="63%">
Retrieves the text for the submit button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f57b247c-bd6d-46ea-be95-a239c1b087ce">GetTooltipText</a>
</td>
<td align="left" width="63%">
Retrieves the tooltip text displayed for a control.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f58529da-f419-445a-879a-2c087b770f0f">Interfaces</a>
 

 

