---
UID: NF:encdec.IXDSCodecConfig.SetPauseBufferTime
title: IXDSCodecConfig::SetPauseBufferTime
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\ixdscodecconfig_setpausebuffertime.htm
old-project: mstv
ms.assetid: 46e71958-86bc-4649-a401-b16131dd6bbd
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IXDSCodecConfig interface [Microsoft TV Technologies],SetPauseBufferTime method, IXDSCodecConfig.SetPauseBufferTime, IXDSCodecConfig::SetPauseBufferTime, IXDSCodecConfigSetPauseBufferTime, SetPauseBufferTime, SetPauseBufferTime method [Microsoft TV Technologies], SetPauseBufferTime method [Microsoft TV Technologies],IXDSCodecConfig interface, encdec/IXDSCodecConfig::SetPauseBufferTime, mstv.ixdscodecconfig_setpausebuffertime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: encdec.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: ProtType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EncDec.h
api_name:
 - IXDSCodecConfig.SetPauseBufferTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IXDSCodecConfig::SetPauseBufferTime


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>SetPauseBufferTime</b> method specifies how often the XDS Codec filter attempts to generate a new license for protected video content.


## -parameters




### -param dwPauseBufferTime [in]

Specifies the license generation interval, in seconds.


## -returns



Returns an <b>HRESULT</b>.




## -see-also




<a href="https://msdn.microsoft.com/90f8ce9b-2a85-43d0-9f2a-a3d248414a2d">IXDSCodecConfig Interface</a>
 

 

