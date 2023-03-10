---
UID: NF:appxpackaging.IAppxBlockMapReader.GetHashMethod
title: IAppxBlockMapReader::GetHashMethod (appxpackaging.h)
description: Retrieves the URI for the hash algorithm used to create block hashes in the block map.
helpviewer_keywords: ["GetHashMethod","GetHashMethod method [App packaging and management]","GetHashMethod method [App packaging and management]","IAppxBlockMapReader interface","IAppxBlockMapReader interface [App packaging and management]","GetHashMethod method","IAppxBlockMapReader.GetHashMethod","IAppxBlockMapReader::GetHashMethod","appxpackaging/IAppxBlockMapReader::GetHashMethod","appxpkg.iappxblockmapreader_gethashmethod"]
old-location: appxpkg\iappxblockmapreader_gethashmethod.htm
tech.root: appxpkg
ms.assetid: 661E4F12-E426-4811-81FA-4F065C6E488A
ms.date: 12/05/2018
ms.keywords: GetHashMethod, GetHashMethod method [App packaging and management], GetHashMethod method [App packaging and management],IAppxBlockMapReader interface, IAppxBlockMapReader interface [App packaging and management],GetHashMethod method, IAppxBlockMapReader.GetHashMethod, IAppxBlockMapReader::GetHashMethod, appxpackaging/IAppxBlockMapReader::GetHashMethod, appxpkg.iappxblockmapreader_gethashmethod
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
 - IAppxBlockMapReader::GetHashMethod
 - appxpackaging/IAppxBlockMapReader::GetHashMethod
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
 - IAppxBlockMapReader.GetHashMethod
---

# IAppxBlockMapReader::GetHashMethod


## -description

Retrieves the URI for the hash algorithm used to create block hashes in the block map.

## -parameters

### -param hashMethod [out, retval]

Type: <b><a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775038(v=vs.85)">IUri</a>**</b>

The hash algorithm used in this block map.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <i>hashMethod</i> value corresponds to the <b>HashMethod</b> attribute of the <a href="/uwp/schemas/blockmapschema/element-blockmap">BlockMap</a> root element. 

<b>GetHashMethod</b> returns supported URIs for <a href="/uwp/schemas/mobilebroadbandschema/carriercontrolsignatureschema/element-digestmethod">DigestMethod</a>s.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapreader">IAppxBlockMapReader</a>