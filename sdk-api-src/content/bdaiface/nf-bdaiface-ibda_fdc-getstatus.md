---
UID: NF:bdaiface.IBDA_FDC.GetStatus
title: IBDA_FDC::GetStatus
author: windows-sdk-content
description: Gets the tuning status of the Forward Data Channel (FDC) stream.
old-location: mstv\ibda_fdc_getstatus.htm
tech.root: mstv
ms.assetid: feaa3d72-353f-45ed-b458-7345bbe07dd2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetStatus, GetStatus method [Microsoft TV Technologies], GetStatus method [Microsoft TV Technologies],IBDA_FDC interface, IBDA_FDC interface [Microsoft TV Technologies],GetStatus method, IBDA_FDC.GetStatus, IBDA_FDC::GetStatus, bdaiface/IBDA_FDC::GetStatus, mstv.ibda_fdc_getstatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
 - bdaiface.h
api_name:
 - IBDA_FDC.GetStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_FDC::GetStatus


## -description


Gets the tuning status of the Forward Data Channel (FDC) stream.


## -parameters




### -param CurrentBitrate [out]

Receives the expected bit rate of the FDC stream, in kilobits per second (kbps). 


### -param CarrierLock [out]

Receives the carrier lock status.


### -param CurrentFrequency [out]

Receives the current frequency of the FDC tuner, in kHz.


### -param CurrentSpectrumInversion [out]

Receives the expected spectrum inversion status of the FDC stream.


### -param CurrentPIDList [out]

Receives a comma-separated list of packet identifiers (PIDs). The caller must release the string by calling <b>SysFreeString</b>.


### -param CurrentTIDList [out]

Receives a comma-separated list of table identifiers (TIDs). The caller must release the string by calling <b>SysFreeString</b>.


### -param Overflow [out]

Receives the overflow status.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd693347(v=VS.85).aspx">IBDA_FDC</a>
 

 

