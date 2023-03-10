---
UID: NF:appxpackaging.IAppxBlockMapReader.GetStream
title: IAppxBlockMapReader::GetStream (appxpackaging.h)
description: Retrieves a read-only stream that represents the XML content of the block map.
helpviewer_keywords: ["GetStream","GetStream method [App packaging and management]","GetStream method [App packaging and management]","IAppxBlockMapReader interface","IAppxBlockMapReader interface [App packaging and management]","GetStream method","IAppxBlockMapReader.GetStream","IAppxBlockMapReader::GetStream","appxpackaging/IAppxBlockMapReader::GetStream","appxpkg.iappxblockmapreader_getstream"]
old-location: appxpkg\iappxblockmapreader_getstream.htm
tech.root: appxpkg
ms.assetid: 95EBABDA-45D5-436C-B627-51C14D9091EA
ms.date: 12/05/2018
ms.keywords: GetStream, GetStream method [App packaging and management], GetStream method [App packaging and management],IAppxBlockMapReader interface, IAppxBlockMapReader interface [App packaging and management],GetStream method, IAppxBlockMapReader.GetStream, IAppxBlockMapReader::GetStream, appxpackaging/IAppxBlockMapReader::GetStream, appxpkg.iappxblockmapreader_getstream
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
 - IAppxBlockMapReader::GetStream
 - appxpackaging/IAppxBlockMapReader::GetStream
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
 - IAppxBlockMapReader.GetStream
---

# IAppxBlockMapReader::GetStream


## -description

Retrieves a read-only stream that represents the XML content of the block map.

## -parameters

### -param blockMapStream [out, retval]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>**</b>

A read-only stream that represents the XML content of the block map.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapreader">IAppxBlockMapReader</a>