---
UID: NF:tuner.ITunerCap.get_SupportedVideoFormats
title: ITunerCap::get_SupportedVideoFormats
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\itunercap_get_supportedvideoformats.htm
tech.root: mstv
ms.assetid: 301402bd-8c9c-4dab-a00b-29aaa8efb2a2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITunerCap interface [Microsoft TV Technologies],get_SupportedVideoFormats method, ITunerCap.get_SupportedVideoFormats, ITunerCap::get_SupportedVideoFormats, ITunerCapget_SupportedVideoFormats, get_SupportedVideoFormats, get_SupportedVideoFormats method [Microsoft TV Technologies], get_SupportedVideoFormats method [Microsoft TV Technologies],ITunerCap interface, mstv.itunercap_get_supportedvideoformats, tuner/ITunerCap::get_SupportedVideoFormats
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - ITunerCap.get_SupportedVideoFormats
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tuner.h
: 
- ITunerCap.get_SupportedVideoFormats
: 
---

# ITunerCap::get_SupportedVideoFormats


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_SupportedVideoFormats</b> method retrieves the video formats that are supported by the TV tuner.


## -parameters




### -param pulAMTunerModeType [out]

Receives a bitmask that indicates the frequency ranges that are supported by the BDA device filter. For a list of valid mask bits, see <a href="https://msdn.microsoft.com/ce5e6f6d-da79-4a86-abd4-bb28e66d5947">AMTunerModeType Enumeration</a>.


### -param pulAnalogVideoStandard [out]

Receives a bitmask that indicates the analog television signal formats that are supported by the BDA device filter. For a list of valid mask bits, see <a href="https://msdn.microsoft.com/6760a40c-550c-4774-a5d1-d7e2a6aa6096">AnalogVideoStandard Enumeration</a>.


## -returns



When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d7027ff4-4fb9-48c1-b527-92e65009b089">ITunerCap Interface</a>
 

 

