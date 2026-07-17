---
UID: NF:appxpackaging.IAppxBundleReader2.GetPayloadPackageReader
tech.root: appxpkg
title: IAppxBundleReader2::GetPayloadPackageReader
ms.date: 01/06/2026
targetos: Windows
description: Creates an instance of [IAppxPackageReader](nn-appxpackaging-iappxpackagereader.md) for reading the contents of a bundle's payload file.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: appxpackaging.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 version 26100
req.target-min-winversvr: Windows Server 2025
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - appxpackaging.h
api_name:
 - IAppxBundleReader2::GetPayloadPackageReader
f1_keywords:
 - IAppxBundleReader2::GetPayloadPackageReader
 - appxpackaging/IAppxBundleReader2::GetPayloadPackageReader
dev_langs:
 - c++
helpviewer_keywords:
 - GetPayloadPackageReader
---

## -description

Creates an instance of [IAppxPackageReader](nn-appxpackaging-iappxpackagereader.md) for reading the contents of a bundle's payload file.

## -parameters

### -param fileName [in]

An LPCWSTR containing the file name of the package to read.

### -param payloadPackageReader [out]

Receives the created **IAppxPackageReader** instance.

## -returns

If the method succeeds, it returns **S_OK**. Otherwise, it returns an error code that includes, but is not limited to, those in the following table. 

| Return code                              | Description                                            |
|------------------------------------------|--------------------------------------------------------|
| HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) | There is no package file with the specified file name. |
| E_POINTER                                | The *fileName* or *payloadPackageReader* param is NULL.|

## -remarks

## -see-also

