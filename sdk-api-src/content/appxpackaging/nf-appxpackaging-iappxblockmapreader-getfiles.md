---
UID: NF:appxpackaging.IAppxBlockMapReader.GetFiles
title: IAppxBlockMapReader::GetFiles (appxpackaging.h)
description: Retrieves an enumerator for traversing the files listed in the block map.
helpviewer_keywords: ["GetFiles","GetFiles method [App packaging and management]","GetFiles method [App packaging and management]","IAppxBlockMapReader interface","IAppxBlockMapReader interface [App packaging and management]","GetFiles method","IAppxBlockMapReader.GetFiles","IAppxBlockMapReader::GetFiles","appxpackaging/IAppxBlockMapReader::GetFiles","appxpkg.iappxblockmapreader_getfiles"]
old-location: appxpkg\iappxblockmapreader_getfiles.htm
tech.root: appxpkg
ms.assetid: 7E46C555-8C61-4F26-9732-07E0DEEAF66F
ms.date: 12/05/2018
ms.keywords: GetFiles, GetFiles method [App packaging and management], GetFiles method [App packaging and management],IAppxBlockMapReader interface, IAppxBlockMapReader interface [App packaging and management],GetFiles method, IAppxBlockMapReader.GetFiles, IAppxBlockMapReader::GetFiles, appxpackaging/IAppxBlockMapReader::GetFiles, appxpkg.iappxblockmapreader_getfiles
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
 - IAppxBlockMapReader::GetFiles
 - appxpackaging/IAppxBlockMapReader::GetFiles
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
 - IAppxBlockMapReader.GetFiles
---

# IAppxBlockMapReader::GetFiles


## -description

Retrieves an enumerator for traversing the files listed in the block map.

## -parameters

### -param enumerator [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfilesenumerator">IAppxBlockMapFilesEnumerator</a>**</b>

The enumerator of all the files listed in the block map.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapreader">IAppxBlockMapReader</a>