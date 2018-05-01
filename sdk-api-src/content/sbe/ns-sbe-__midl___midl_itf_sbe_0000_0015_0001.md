---
UID: NS:sbe.__MIDL___MIDL_itf_sbe_0000_0015_0001
title: "__MIDL___MIDL_itf_sbe_0000_0015_0001"
author: windows-driver-content
description: Describes a stream produced by the stream buffer engine.
old-location: mstv\sbe2_stream_desc.htm
old-project: mstv
ms.assetid: ab7ccd5b-1ac8-4d33-aea6-49383025270b
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: SBE2_STREAM_DESC, SBE2_STREAM_DESC structure [Microsoft TV Technologies], SBE2_STREAM_DESC_VERSION, __MIDL___MIDL_itf_sbe_0000_0015_0001, mstv.sbe2_stream_desc, sbe/SBE2_STREAM_DESC
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SBE2_STREAM_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	sbe.h
api_name:
-	SBE2_STREAM_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# __MIDL___MIDL_itf_sbe_0000_0015_0001 structure


## -description


Describes a stream produced by the stream buffer engine.


## -struct-fields




### -field Version

The version number of the stream. Currently the following value is defined.

<a id="SBE2_STREAM_DESC_VERSION"></a>
<a id="sbe2_stream_desc_version"></a>


#### SBE2_STREAM_DESC_VERSION


### -field StreamId

The identifier of the stream.


### -field Default

Specifies whether the steam is the default for the current media type. If the value is nonzero, the stream is the default. If the value is zero, the stream is not the default.


### -field Reserved

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/77a918f8-d305-4d4d-9a5c-523ddb796b26">ISBE2EnumStream</a>



<a href="https://msdn.microsoft.com/90ac310a-7fd3-440f-9cf7-7d6eb58996cc">Stream Buffer Engine Structures</a>
 

 

