---
UID: NF:cfapi.CfGetSyncRootInfoByHandle
title: CfGetSyncRootInfoByHandle function (cfapi.h)
description: Gets various characteristics of the sync root containing a given file specified by a file handle.
helpviewer_keywords: ["CfGetSyncRootInfoByHandle","CfGetSyncRootInfoByHandle function","cfapi/CfGetSyncRootInfoByHandle","cloudApi.cfgetsyncrootinfobyhandle"]
old-location: cloudapi\cfgetsyncrootinfobyhandle.htm
tech.root: cloudapi
ms.assetid: EC96CB4E-6BCE-49D9-9CDA-A24A9303B5CF
ms.date: 12/05/2018
ms.keywords: CfGetSyncRootInfoByHandle, CfGetSyncRootInfoByHandle function, cfapi/CfGetSyncRootInfoByHandle, cloudApi.cfgetsyncrootinfobyhandle
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CfGetSyncRootInfoByHandle
 - cfapi/CfGetSyncRootInfoByHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfGetSyncRootInfoByHandle
---

# CfGetSyncRootInfoByHandle function


## -description

Gets various characteristics of the sync root containing a given file specified by a file handle.

## -parameters

### -param FileHandle [in]

Handle of the file under the sync root whose information is to be queried.

### -param InfoClass [in]

Types of sync root information.

### -param InfoBuffer [out]

A pointer to a buffer that will receive the sync root information.

### -param InfoBufferLength [in]

Length, in bytes, of the <i>InfoBuffer</i>.

### -param ReturnedLength [out, optional]

The number of bytes returned in the <i>InfoBuffer</i>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Unlike most placeholder APIs that take a file handle, this one does not modify the file in any way, therefore the file handle only requires READ_ATTRIBUTES access.

