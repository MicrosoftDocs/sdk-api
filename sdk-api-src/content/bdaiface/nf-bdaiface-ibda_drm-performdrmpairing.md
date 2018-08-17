---
UID: NF:bdaiface.IBDA_DRM.PerformDRMPairing
title: IBDA_DRM::PerformDRMPairing
author: windows-sdk-content
description: The PerformDRMPairing method requests the tuner to perform a DRM handshake with the user's computer.
old-location: mstv\ibda_drm_performdrmpairing.htm
old-project: mstv
ms.assetid: a3cd9e0c-cfb1-445f-bafc-c1a4f24550f8
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_DRM interface [Microsoft TV Technologies],PerformDRMPairing method, IBDA_DRM.PerformDRMPairing, IBDA_DRM::PerformDRMPairing, IBDA_DRMPerformDRMPairing, PerformDRMPairing, PerformDRMPairing method [Microsoft TV Technologies], PerformDRMPairing method [Microsoft TV Technologies],IBDA_DRM interface, bdaiface/IBDA_DRM::PerformDRMPairing, mstv.ibda_drm_performdrmpairing
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdaiface.h
api_name:
 - IBDA_DRM.PerformDRMPairing
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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



If you call this method asynchronously (<i>fSync</i> equal to <b>FALSE</b>), you can poll the status of the operation by calling <a href="https://msdn.microsoft.com/en-us/library/Dd693319(v=VS.85).aspx">IBDA_DRM::GetDRMPairingStatus</a>. While the operation is in progress, <b>GetDRMPairingStatus</b> returns S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd693315(v=VS.85).aspx">IBDA_DRM Interface</a>
 

 

