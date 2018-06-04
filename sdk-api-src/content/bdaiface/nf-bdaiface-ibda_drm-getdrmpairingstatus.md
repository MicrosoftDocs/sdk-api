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

# IBDA_DRM::GetDRMPairingStatus


## -description


The <b>GetDRMPairingStatus</b> method queries the status of the DRM handshake.


## -parameters




### -param pdwStatus [out]

Receives a value from the <a href="https://msdn.microsoft.com/d1b100e5-497e-4cb1-9cb8-38424c9eecf8">BDA_DrmPairingError</a> enumeration.


### -param phError






#### - phErrort [out]

Receives an <b>HRESULT</b> value indicating the success or failure of the DRM handshake.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The device does not support this functionality, or the handshake is still in progress.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d0bde207-d550-4e98-85c7-b0d47b0cd637">IBDA_DRM Interface</a>
 

 

