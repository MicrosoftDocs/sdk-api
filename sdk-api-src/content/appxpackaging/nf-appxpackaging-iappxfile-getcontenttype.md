---
UID: NF:appxpackaging.IAppxFile.GetContentType
title: IAppxFile::GetContentType (appxpackaging.h)
description: Retrieves the content type of the file.
helpviewer_keywords: ["GetContentType","GetContentType method [App packaging and management]","GetContentType method [App packaging and management]","IAppxFile interface","IAppxFile interface [App packaging and management]","GetContentType method","IAppxFile.GetContentType","IAppxFile::GetContentType","appxpackaging/IAppxFile::GetContentType","appxpkg.iappxfile_getcontenttype"]
old-location: appxpkg\iappxfile_getcontenttype.htm
tech.root: appxpkg
ms.assetid: 86EE47E1-B2AD-4610-8C9A-679536F9C51D
ms.date: 12/05/2018
ms.keywords: GetContentType, GetContentType method [App packaging and management], GetContentType method [App packaging and management],IAppxFile interface, IAppxFile interface [App packaging and management],GetContentType method, IAppxFile.GetContentType, IAppxFile::GetContentType, appxpackaging/IAppxFile::GetContentType, appxpkg.iappxfile_getcontenttype
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
 - IAppxFile::GetContentType
 - appxpackaging/IAppxFile::GetContentType
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
 - IAppxFile.GetContentType
---

# IAppxFile::GetContentType


## -description

Retrieves the content type of the file.

## -parameters

### -param contentType [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a>*</b>

The content type of the file.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The caller is responsible for deallocating the memory used by <i>contentType</i>. Use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to deallocate the string's memory.


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-extract-content-from-a-package">Quickstart: Extract app package contents</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfile">IAppxFile</a>