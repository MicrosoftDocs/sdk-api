---
UID: NF:cfapi.CfGetSyncRootInfoByPath
title: CfGetSyncRootInfoByPath function (cfapi.h)
description: Gets various sync root information given a file under the sync root.
helpviewer_keywords: ["CfGetSyncRootInfoByPath","CfGetSyncRootInfoByPath function","cfapi/CfGetSyncRootInfoByPath","cloudApi.cfgetsyncrootinfobypath"]
old-location: cloudapi\cfgetsyncrootinfobypath.htm
tech.root: cloudapi
ms.assetid: 0FEEF910-3545-4D94-BFF9-88AEE084F454
ms.date: 12/05/2018
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

A fully qualified path to a file whose sync root information is to be queried

### -param InfoClass [in]

Types of sync root information.

### -param InfoBuffer [out]

A pointer to a buffer that will receive the sync root information.

### -param InfoBufferLength [in]

Length, in bytes, of the <i>InfoBuffer</i>.

### -param ReturnedLength [out, optional]

Length, in bytes, of the returned sync root information. Refer to <a href="/windows/desktop/api/cfapi/nf-cfapi-cfregistersyncroot">CfRegisterSyncRoot</a> for details about the sync root information.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.