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

# ITfIntegratableCandidateListUIElement::OnKeyDown


## -description


Processes a key press.


## -parameters




### -param wParam [in]

Specifies the virtual-key code of the key. For more information about this parameter, see the <i>wParam</i> parameter in <a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a>.


### -param lParam [in]

Specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag of the key. For more information about this parameter, see the <i>lParam</i> parameter in <a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a>.


### -param pfEaten [out]

<b>TRUE</b> if the key event was handled; otherwise, <b>FALSE</b>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/684d3c01-fa95-4a19-b5fb-48a62315ce2f">OnKeyDown</a> method enables an app to ask query the text service if it wants to process a given key in an integration style.  The behavior of the <b>OnKeyDown</b> method can depend on the integration style. If the text service returns <i>*pfEaten</i>=<b>TRUE</b>, then the app should do
    no processing of the key. If <b>FALSE</b> is returned, the app can perform its own action in response to the key.

<b>GUID_INTEGRATIONSTYLE_SEARCHBOX</b> ({E6D1BD11-82F7-4903-AE21-1A6397CDE2EB}) enables an implementation of a keyboarding experience in which the user can move perceived keyboard focus 
    from the search box to the candidate list to search suggestions. The text service can process keys     like <b>VK_UP</b> and <b>VK_DOWN</b> before Search handles them to change its internal state.




## -see-also




<a href="https://msdn.microsoft.com/F9AB2037-6806-42FC-BD41-F6B6BA047908">ITfIntegratableCandidateListUIElement</a>
 

 

