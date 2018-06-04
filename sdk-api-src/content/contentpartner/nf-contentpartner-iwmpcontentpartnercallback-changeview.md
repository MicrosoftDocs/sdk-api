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

# IWMPContentPartnerCallback::ChangeView


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>ChangeView</b> method changes the view in Windows Media Player.




## -parameters




### -param bstrType [in]

A <a href="https://msdn.microsoft.com/88ff9b91-6b21-4f7d-ae13-e8456a3e0f75">library location constant</a> that specifies the type of the new library view. For example, the constant g_szGenreID specifies that the new view will show a particular genre.


### -param bstrID [in]

The ID of the specific item to show in the new view. For example, if <i>bstrType</i> is g_szGenreID, then this parameter specifies the ID of the particular genre to show in the new view.


### -param bstrFilter [in]

The filter for the new view. The view will be filtered as if the user had entered this text in the Player's word wheel control.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This method must be called only in response to a user request, such as when the user invokes a command by clicking a context menu item.




## -see-also




<a href="https://msdn.microsoft.com/3c66052b-2b82-44aa-868d-5d5a4501c457">IWMPContentPartnerCallback Interface</a>
 

 

