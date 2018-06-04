---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IFECommon interface


## -description


The <b>IFECommon</b> interface provides IME-related services that are common for different languages.

<b>IFECommon</b> allows the developer to control very basic functions of IMEs.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFECommon</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFECommon</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFECommon</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E70E3B78-58D7-40E9-8DAB-447B4CBC13F4">InvokeDictToolDialog</a>
</td>
<td align="left" width="63%">
Invokes the Microsoft IME's Dictionary Tool from the app.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FBD09E98-9C89-4CE4-9D17-A13E2BE0AB91">InvokeWordRegDialog</a>
</td>
<td align="left" width="63%">
Invokes the Microsoft IME Word Register Dialog Window from the app.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FFC3E200-54D4-4C47-A4A3-87AA2A4A2232">IsDefaultIME</a>
</td>
<td align="left" width="63%">
Determines if the IME specified by the class ID is the default IME on a local computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D54AABA7-8FAC-4867-91E7-BAF477F8DAB9">SetDefaultIME</a>
</td>
<td align="left" width="63%">
Allows the Microsoft IME to become the default IME in the keyboard layout.

</td>
</tr>
</table> 


## -remarks



Create an instance of this interface with the <a href="https://msdn.microsoft.com/A8A0CCC4-0A60-4E2A-9E6D-DC2C614B631D">CreateIFECommonInstance</a> function.



