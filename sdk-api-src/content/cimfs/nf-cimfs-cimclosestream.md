---
UID: NF:cimfs.CimCloseStream
title: CimCloseStream
description: The CimCloseStream function frees resources associated with the stream handle.
ms.date: 08/01/2022
tech.root: cimfs
ms.keywords: CimCloseStream
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: cimfs.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: cimfs.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - cimfs.h
api_name:
 - CimCloseStream
f1_keywords:
 - CimCloseStream
 - cimfs/CimCloseStream
---

## -description

Frees resources associated with the stream handle.

## -parameters

### -param cimStreamHandle

Type: **CIMFS_STREAM_HANDLE**

An opaque handle that represents a writer for the stream created with CimCreateFile or CimCreateAlternateStream.

## -remarks

## -see-also
