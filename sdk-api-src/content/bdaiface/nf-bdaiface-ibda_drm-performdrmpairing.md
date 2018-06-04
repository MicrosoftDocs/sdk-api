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

# IBDA_DRM::PerformDRMPairing


## -description


The <b>PerformDRMPairing</b> method requests the tuner to perform a DRM handshake with the user's computer.


## -parameters




### -param fSync [in]

If <b>TRUE</b>, the method blocks until the operation is completed. If <b>FALSE</b>, the operation is completed asynchronously.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



If you call this method asynchronously (<i>fSync</i> equal to <b>FALSE</b>), you can poll the status of the operation by calling <a href="https://msdn.microsoft.com/dff38609-9e90-491c-b8c4-33fd07471895">IBDA_DRM::GetDRMPairingStatus</a>. While the operation is in progress, <b>GetDRMPairingStatus</b> returns S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/d0bde207-d550-4e98-85c7-b0d47b0cd637">IBDA_DRM Interface</a>
 

 

