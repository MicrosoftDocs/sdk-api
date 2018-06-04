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

# IWMPContentPartnerCallback::ShowPopup


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>ShowPopup</b> method instructs Windows Media Player to display an HTML-based dialog box that hosts a webpage provided by the online store.




## -parameters




### -param lIndex [in]

Index, meaningful only to the online store, of the webpage to display in the dialog box.


### -param bstrParameters [in]

Parameters associated with the dialog box.


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



Windows Media Player calls <a href="https://msdn.microsoft.com/b7355c45-fb58-45f4-b7e4-3dd2c3f8c918">IWMPContentPartner::GetItemInfo</a>, passing the value of <i>lIndex</i> in the <i>pContext</i> parameter, to retrieve a URL. Windows Media Player then appends the value of <i>bstrParameters</i> to the URL, and uses the URL, along with the appended parameters, to retrieve the webpage to display in the dialog box.

You can use the <i>bstrParameters</i> parameter to specify the size of the pop-up window. For example, if you set <i>bstrParameters</i> to "DlgX=800&amp;DlgY=400", the pop-up window will have a size of 800 pixels by 400 pixels.




## -see-also




<a href="https://msdn.microsoft.com/3c66052b-2b82-44aa-868d-5d5a4501c457">IWMPContentPartnerCallback Interface</a>
 

 

