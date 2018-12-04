---
UID: NF:bdaiface.IBDA_Encoder.QueryCapabilities
title: IBDA_Encoder::QueryCapabilities
author: windows-sdk-content
description: Gets the number of encoding formats supported by the device.
old-location: mstv\ibda_encoder_querycapabilities.htm
tech.root: mstv
ms.assetid: 038f9360-0515-4655-9397-cd1bfb6c3d21
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IBDA_Encoder interface [Microsoft TV Technologies],QueryCapabilities method, IBDA_Encoder.QueryCapabilities, IBDA_Encoder::QueryCapabilities, QueryCapabilities, QueryCapabilities method [Microsoft TV Technologies], QueryCapabilities method [Microsoft TV Technologies],IBDA_Encoder interface, bdaiface/IBDA_Encoder::QueryCapabilities, mstv.ibda_encoder_querycapabilities
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
 - IBDA_Encoder.QueryCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_Encoder::QueryCapabilities


## -description


Gets the number of encoding formats supported by the device.


## -parameters




### -param NumAudioFmts [out]

Receives the number of audio formats.


### -param NumVideoFmts [out]

Receives the number of video formats.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/43ed9d91-c769-4fb3-bcd9-e5239ec5d9c7">IBDA_Encoder</a>
 

 

