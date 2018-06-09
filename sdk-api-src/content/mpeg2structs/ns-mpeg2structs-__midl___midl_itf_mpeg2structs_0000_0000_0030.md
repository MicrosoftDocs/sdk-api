---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0030
title: "__MIDL___MIDL_itf_mpeg2structs_0000_0000_0030"
author: windows-sdk-content
description: The MPEG_CONTEXT structure identifies the source of an MPEG-2 data stream.
old-location: mstv\mpeg_context.htm
old-project: mstv
ms.assetid: 7a92e545-805b-4ce6-bbf1-397f7a5f6524
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: "*PMPEG_CONTEXT, MPEG_CONTEXT, MPEG_CONTEXT structure [Microsoft TV Technologies], __MIDL___MIDL_itf_mpeg2structs_0000_0000_0030, mpeg2structs/MPEG_CONTEXT, mstv.mpeg_context"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mpeg2structs.h
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
req.typenames: MPEG_CONTEXT, *PMPEG_CONTEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mpeg2Structs.h
api_name:
 - MPEG_CONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_mpeg2structs_0000_0000_0030 structure


## -description



The <b>MPEG_CONTEXT</b> structure identifies the source of an MPEG-2 data stream.




## -struct-fields




### -field Type

Specifies the source type, as an <a href="https://msdn.microsoft.com/cb76873e-78d0-4fd2-9caa-bff4ae250073">MPEG_CONTEXT_TYPE</a> value. Currently, the value must be MPEG_CONTEXT_BCS_DEMUX.


### -field U

A union that contains the following members.


### -field U.Demux

Specifies an <a href="https://msdn.microsoft.com/ecc4f3bb-16f5-4398-bcd5-3316da8529ec">MPEG_BCS_DEMUX</a> structure that identifies the filter graph instance.


### -field U.Winsock

Currently not supported.


## -see-also




<a href="https://msdn.microsoft.com/5ae43ac6-519d-486b-aaa5-c766f3194ef2">BDA Structures</a>
 

 

