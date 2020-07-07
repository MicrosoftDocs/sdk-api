---
UID: NA:cimfs
title: cimfs
ms.date: 9/9/2019
ms.keywords: cimfs
ms.topic: language-reference
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: apiset
req.ddi-compliance: 
req.dll: 
req.header: cimfs.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - cimfs.h
api_name:
 - cimfs
---

## -description

Provides the ability to construct and mount Composite Images (CIMs).

## -remarks
A CIM is a file-backed image format similar in concept to a WIM or a read-only VHD.

A CIM image consists of a small collection of flat files that include one or more data and metadata region files, one or more object ID files and one or more filesystem description files. As a result of their “flatness” CIMs are faster to construct, extract and delete than the equivalent raw directories they contain.

CIMs are composite in that a given image can contain multiple file system volumes which can be mounted individually while sharing the same data region backing files.

CIMs support deduplication at the file level. The CIMFS file system supports many of the constructs of NTFS such as security descriptors, alternate data streams, hard links and reparse points.

Once constructed, a CIM can be mounted with the support of the CIMFS driver. The mount constructs a read-only disk and file system volume device for the image. The contents of a mounted CIM can be accessed read-only using the standard Win32 or NT API file system interface.

CIMs were designed and optimized to be used as a Windows Container image layout.

## -see-also

## -examples

