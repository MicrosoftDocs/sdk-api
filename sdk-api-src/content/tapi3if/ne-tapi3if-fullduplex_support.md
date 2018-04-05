---
UID: NE:tapi3if.FULLDUPLEX_SUPPORT
title: FULLDUPLEX_SUPPORT
author: windows-driver-content
description: The FULLDUPLEX_SUPPORT enum is used by applications interacting with legacy TSPs to indicate whether a specified terminal supports full duplex operations. This enum is returned by the ITLegacyWaveSupport::IsFullDuplex method.
old-location: tapi3\fullduplex_support.htm
old-project: Tapi
ms.assetid: 36f9f126-361f-448a-a464-ffef1de25d26
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: FDS_NOTSUPPORTED, FDS_SUPPORTED, FDS_UNKNOWN, FULLDUPLEX_SUPPORT, FULLDUPLEX_SUPPORT enumeration [TAPI 2.2], _tapi3_fullduplex_support, tapi3.fullduplex_support, tapi3if/FDS_NOTSUPPORTED, tapi3if/FDS_SUPPORTED, tapi3if/FDS_UNKNOWN, tapi3if/FULLDUPLEX_SUPPORT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: tapi3if.h
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
req.typenames: FULLDUPLEX_SUPPORT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi3if.h
api_name:
-	FULLDUPLEX_SUPPORT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# FULLDUPLEX_SUPPORT enumeration


## -description


The 
<b>FULLDUPLEX_SUPPORT</b> enum is used by applications interacting with legacy TSPs to indicate whether a specified terminal supports full duplex operations. This enum is returned by the 
<a href="https://msdn.microsoft.com/117586d7-8214-4fc8-9c7d-08865582cc2a">ITLegacyWaveSupport::IsFullDuplex</a> method.


## -enum-fields




### -field FDS_SUPPORTED

Full duplex supported.


### -field FDS_NOTSUPPORTED

Full duplex not supported.


### -field FDS_UNKNOWN

The TSP cannot determine whether the device is full duplex.


## -see-also




<a href="https://msdn.microsoft.com/117586d7-8214-4fc8-9c7d-08865582cc2a">ITLegacyWaveSupport::IsFullDuplex</a>
 

 

