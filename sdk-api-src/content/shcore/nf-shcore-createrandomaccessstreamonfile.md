---
UID: NF:shcore.CreateRandomAccessStreamOnFile
title: CreateRandomAccessStreamOnFile function (shcore.h)
description: Creates a Windows Runtime random access stream for a file.
helpviewer_keywords: ["CreateRandomAccessStreamOnFile","CreateRandomAccessStreamOnFile function [Windows Runtime]","shcore/CreateRandomAccessStreamOnFile","winrt.createrandomaccessstreamonfile"]
old-location: winrt\createrandomaccessstreamonfile.htm
tech.root: WinRT
ms.assetid: 6D3D2B25-7373-4BA5-BF6B-FB461C2DE982
ms.date: 12/05/2018
ms.keywords: CreateRandomAccessStreamOnFile, CreateRandomAccessStreamOnFile function [Windows Runtime], shcore/CreateRandomAccessStreamOnFile, winrt.createrandomaccessstreamonfile
req.header: shcore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shcore.lib
req.dll: Shcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateRandomAccessStreamOnFile
 - shcore/CreateRandomAccessStreamOnFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - shcore.dll
 - API-MS-Win-ShCore-stream-WinRT-l1-1-0.dll
api_name:
 - CreateRandomAccessStreamOnFile
---

# CreateRandomAccessStreamOnFile function


## -description

Creates a  Windows Runtime random access stream for a file.

## -parameters

### -param filePath [in]

The fully qualified path of the file to encapsulate.

### -param accessMode [in]

An <a href="/uwp/api/Windows.Storage.FileAccessMode">AccessMode</a> value that specifies the behavior of the <a href="/uwp/api/windows.storage.streams.randomaccessstream">RandomAccessStream</a> that encapsulates the file.

### -param riid [in]

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_RandomAccessStream.

### -param ppv [out]

When this method returns successfully, contains the interface pointer requested in <i>riid</i>, typically the <a href="/previous-versions/hh438400(v=vs.85)">IRandomAccessStream</a> that encapsulates the file.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Use the <b>CreateRandomAccessStreamOnFile</b> function to create a <a href="/uwp/api/windows.storage.streams.randomaccessstream">RandomAccessStream</a> that encapsulates a file.

We recommend that you use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args">IID_PPV_ARGS</a> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.

## -see-also

<a href="/windows/desktop/api/shcore/nf-shcore-createrandomaccessstreamoverstream">CreateRandomAccessStreamOverStream</a>



<a href="/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream">CreateStreamOverRandomAccessStream</a>



<a href="/uwp/api/windows.storage.streams.randomaccessstream">RandomAccessStream</a>