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

# ITfUIElementSink::BeginUIElement


## -description


The <b>ITfUIElementSink::BeginUIElement</b> method is called when the UIElement started. This sink can let the textservice to draw or not to draw the UI element.


## -parameters




### -param dwUIElementId [in]

[in] Id of the UIElement that was started.


### -param pbShow

[in, out] Return <b>true</b> if the application does not draw the UIElement content and the text service draws its original UI content. Return <b>false</b> if the application draws the UIElement's content and stops the text service from drawing it. The application can get the <a href="https://msdn.microsoft.com/651c3ca1-5e5b-4978-80d2-2183bd158610">ITfUIElement</a> interface by using <a href="https://msdn.microsoft.com/e3a2a7ae-1ca2-4c1e-83af-207821966147">ITfUIElementMgr::GetUIElement</a> and it can evaluate if it can handle the UIElement by QI with <b>IID_ITfCandidateListUIElement</b> or with other UIElement interfaces. The application can always return <b>FALSE</b> if it is unknown or it cannot be handled. In this case, the text service will not show any extra UI on the screen. This is a good way for some full screen applications. Alternatively, the application can return <b>TRUE</b> to use TextService's UI on some particular or unknown UIs.


## -returns



The TSF manager ignores the return value of this method.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 



