---
UID: NF:cfapi.CfGetSyncRootInfoByPath
title: CfGetSyncRootInfoByPath function (cfapi.h)
description: Gets various sync root information given a file under the sync root.
helpviewer_keywords: ["CfGetSyncRootInfoByPath","CfGetSyncRootInfoByPath function","cfapi/CfGetSyncRootInfoByPath","cloudApi.cfgetsyncrootinfobypath"]
old-location: cloudapi\cfgetsyncrootinfobypath.htm
tech.root: cloudapi
ms.assetid: 0FEEF910-3545-4D94-BFF9-88AEE084F454
ms.date: 03/30/2023
ms.keywords: CfGetSyncRootInfoByPath, CfGetSyncRootInfoByPath function, cfapi/CfGetSyncRootInfoByPath, cloudApi.cfgetsyncrootinfobypath
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
 - CfGetSyncRootInfoByPath
 - cfapi/CfGetSyncRootInfoByPath
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
 - CfGetSyncRootInfoByPath
---

# CfGetSyncRootInfoByPath function

## -description

Gets various sync root information given a file under the sync root.

## -parameters

### -param FilePath [in]

A fully qualified path to a file whose sync root information is to be queried.

### -param InfoClass [in]

Types of sync root information.

### -param InfoBuffer [out]

A pointer to a buffer that will receive the sync root information.

### -param InfoBufferLength [in]

Length, in bytes, of the *InfoBuffer*.

### -param ReturnedLength [out, optional]

Length, in bytes, of the returned sync root information. Refer to [CfRegisterSyncRoot](nf-cfapi-cfregistersyncroot.md) for details about the sync root information.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

If the file is not underneath a cloud files sync root, the API will fail. On success, information is returned according to the specific *InfoClass* requested.

The *InfoClass* parameter can be one of the following values from [CF_SYNC_ROOT_INFO_CLASS](ne-cfapi-cf_sync_root_info_class.md):

- CF_SYNC_ROOT_INFO_BASIC
- CF_SYNC_ROOT_INFO_STANDARD
- CF_SYNC_ROOT_INFO_PROVIDER

## -see-also

[CfRegisterSyncRoot](nf-cfapi-cfregistersyncroot.md)

[CfGetSyncRootInfoByHandle](nf-cfapi-cfgetsyncrootinfobyhandle.md)
