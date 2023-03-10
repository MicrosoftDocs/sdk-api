---
UID: NS:objidlbase.tagRPCOLEMESSAGE
title: RPCOLEMESSAGE (objidlbase.h)
description: The RPCOLEMESSAGE (objidlbase.h) structure contains marshaling invocation arguments and return values between COM components.
helpviewer_keywords: ["*PRPCOLEMESSAGE","PRPCOLEMESSAGE","PRPCOLEMESSAGE structure pointer [COM]","RPCOLEMESSAGE","RPCOLEMESSAGE structure [COM]","_com_RPCOLEMESSAGE","com.rpcolemessage","objidlbase/PRPCOLEMESSAGE","objidlbase/RPCOLEMESSAGE","tagRPCOLEMESSAGE"]
old-location: com\rpcolemessage.htm
tech.root: com
ms.assetid: b4761462-1910-431c-b5cd-c14fdda0b6b6
ms.date: 08/15/2022
ms.keywords: '*PRPCOLEMESSAGE, PRPCOLEMESSAGE, PRPCOLEMESSAGE structure pointer [COM], RPCOLEMESSAGE, RPCOLEMESSAGE structure [COM], _com_RPCOLEMESSAGE, com.rpcolemessage, objidlbase/PRPCOLEMESSAGE, objidlbase/RPCOLEMESSAGE, tagRPCOLEMESSAGE'
req.header: objidlbase.h
req.include-header: Objidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RPCOLEMESSAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRPCOLEMESSAGE
 - objidlbase/tagRPCOLEMESSAGE
 - RPCOLEMESSAGE
 - objidlbase/RPCOLEMESSAGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidlbase.h
api_name:
 - RPCOLEMESSAGE
---

# RPCOLEMESSAGE structure


## -description

Contains marshaling invocation arguments and return values between COM components.

## -struct-fields

### -field reserved1

This member is reserved.

### -field dataRepresentation

The data representation with which the data was marshaled.

### -field Buffer

A buffer for marshaled data.

### -field cbBuffer

The size of the buffer, in bytes.

### -field iMethod

The number of the method to be invoked.

### -field reserved2

This member is reserved.

### -field rpcFlags

Status flags for the RPC connection.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-irpcchannelbuffer">IRpcChannelBuffer</a>



<a href="/windows/desktop/api/objidl/nn-objidl-irpcstubbuffer">IRpcStubBuffer</a>
