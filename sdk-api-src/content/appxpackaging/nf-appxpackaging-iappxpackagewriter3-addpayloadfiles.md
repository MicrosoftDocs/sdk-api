---
UID: NF:appxpackaging.IAppxPackageWriter3.AddPayloadFiles
title: IAppxPackageWriter3::AddPayloadFiles (appxpackaging.h)
description: Adds one or more payload files to an app package.
helpviewer_keywords: ["AddPayloadFiles","AddPayloadFiles method [App packaging and management]","AddPayloadFiles method [App packaging and management]","IAppxPackageWriter3 interface","IAppxPackageWriter3 interface [App packaging and management]","AddPayloadFiles method","IAppxPackageWriter3.AddPayloadFiles","IAppxPackageWriter3::AddPayloadFiles","appxpackaging/IAppxPackageWriter3::AddPayloadFiles","appxpkg.iappxpackagewriter3_addpayloadfiles"]
old-location: appxpkg\iappxpackagewriter3_addpayloadfiles.htm
tech.root: appxpkg
ms.assetid: 3C798AC2-211B-4735-9860-4F43ADE12F0B
ms.date: 12/05/2018
ms.keywords: AddPayloadFiles, AddPayloadFiles method [App packaging and management], AddPayloadFiles method [App packaging and management],IAppxPackageWriter3 interface, IAppxPackageWriter3 interface [App packaging and management],AddPayloadFiles method, IAppxPackageWriter3.AddPayloadFiles, IAppxPackageWriter3::AddPayloadFiles, appxpackaging/IAppxPackageWriter3::AddPayloadFiles, appxpkg.iappxpackagewriter3_addpayloadfiles
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxPackageWriter3::AddPayloadFiles
 - appxpackaging/IAppxPackageWriter3::AddPayloadFiles
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxPackageWriter3.AddPayloadFiles
---

# IAppxPackageWriter3::AddPayloadFiles


## -description

Adds one or more payload files to an app package.

## -parameters

### -param fileCount [in]

The number of payload files to be added to the app package.

### -param payloadFiles [in]

The payload files to be added.

### -param memoryLimit [in]

The memory limit in bytes.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagewriter3">IAppxPackageWriter3</a>