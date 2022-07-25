---
UID: NF:appxpackaging.IAppxPackageReader.GetPayloadFiles
title: IAppxPackageReader::GetPayloadFiles (appxpackaging.h)
description: Retrieves an enumerator that iterates through the payload files in the package.
helpviewer_keywords: ["GetPayloadFiles","GetPayloadFiles method [App packaging and management]","GetPayloadFiles method [App packaging and management]","IAppxPackageReader interface","IAppxPackageReader interface [App packaging and management]","GetPayloadFiles method","IAppxPackageReader.GetPayloadFiles","IAppxPackageReader::GetPayloadFiles","appxpackaging/IAppxPackageReader::GetPayloadFiles","appxpkg.iappxpackagereader_getpayloadfiles"]
old-location: appxpkg\iappxpackagereader_getpayloadfiles.htm
tech.root: appxpkg
ms.assetid: 20883A4E-BE7B-4312-978A-3BF9362CA6DA
ms.date: 12/05/2018
ms.keywords: GetPayloadFiles, GetPayloadFiles method [App packaging and management], GetPayloadFiles method [App packaging and management],IAppxPackageReader interface, IAppxPackageReader interface [App packaging and management],GetPayloadFiles method, IAppxPackageReader.GetPayloadFiles, IAppxPackageReader::GetPayloadFiles, appxpackaging/IAppxPackageReader::GetPayloadFiles, appxpkg.iappxpackagereader_getpayloadfiles
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IAppxPackageReader::GetPayloadFiles
 - appxpackaging/IAppxPackageReader::GetPayloadFiles
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
 - IAppxPackageReader.GetPayloadFiles
---

# IAppxPackageReader::GetPayloadFiles


## -description

Retrieves an enumerator that iterates through the payload files in the package.

## -parameters

### -param filesEnumerator [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfilesenumerator">IAppxFilesEnumerator</a>**</b>

 An enumerator over all payload files in the package.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagereader">IAppxPackageReader</a>



<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getfootprintfile">IAppxPackageReader::GetFootprintFile</a>



<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getpayloadfile">IAppxPackageReader::GetPayloadFile</a>