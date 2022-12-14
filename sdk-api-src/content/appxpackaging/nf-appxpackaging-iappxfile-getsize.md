---
UID: NF:appxpackaging.IAppxFile.GetSize
title: IAppxFile::GetSize (appxpackaging.h)
description: Retrieves the uncompressed size of the file.
helpviewer_keywords: ["GetSize","GetSize method [App packaging and management]","GetSize method [App packaging and management]","IAppxFile interface","IAppxFile interface [App packaging and management]","GetSize method","IAppxFile.GetSize","IAppxFile::GetSize","appxpackaging/IAppxFile::GetSize","appxpkg.iappxfile_getsize"]
old-location: appxpkg\iappxfile_getsize.htm
tech.root: appxpkg
ms.assetid: 73353CE0-98F8-4A8C-A259-A07C125B9EE9
ms.date: 12/05/2018
ms.keywords: GetSize, GetSize method [App packaging and management], GetSize method [App packaging and management],IAppxFile interface, IAppxFile interface [App packaging and management],GetSize method, IAppxFile.GetSize, IAppxFile::GetSize, appxpackaging/IAppxFile::GetSize, appxpkg.iappxfile_getsize
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
 - IAppxFile::GetSize
 - appxpackaging/IAppxFile::GetSize
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
 - IAppxFile.GetSize
---

# IAppxFile::GetSize


## -description

Retrieves the uncompressed size of the file.

## -parameters

### -param size [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a>*</b>

The uncompressed size, in bytes.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfile">IAppxFile</a>