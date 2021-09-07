---
UID: NF:shcore.CreateStreamOverRandomAccessStream
title: CreateStreamOverRandomAccessStream function (shcore.h)
description: Creates an IStream around a Windows Runtime IRandomAccessStream object.
helpviewer_keywords: ["CreateStreamOverRandomAccessStream","CreateStreamOverRandomAccessStream function [Windows Runtime]","shcore/CreateStreamOverRandomAccessStream","winrt.createstreamoverrandomaccessstream"]
old-location: winrt\createstreamoverrandomaccessstream.htm
tech.root: WinRT
ms.assetid: F9AB8A34-8AB1-4EF1-8659-DAD5713A89BF
ms.date: 12/05/2018
ms.keywords: CreateStreamOverRandomAccessStream, CreateStreamOverRandomAccessStream function [Windows Runtime], shcore/CreateStreamOverRandomAccessStream, winrt.createstreamoverrandomaccessstream
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
req.lib: ShCore.lib
req.dll: ShCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateStreamOverRandomAccessStream
 - shcore/CreateStreamOverRandomAccessStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ShCore.dll
 - API-MS-Win-ShCore-stream-WinRT-l1-1-0.dll
api_name:
 - CreateStreamOverRandomAccessStream
---

# CreateStreamOverRandomAccessStream function


## -description

Creates an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> around a Windows Runtime <a href="/previous-versions/hh438400(v=vs.85)">IRandomAccessStream</a> object.

## -parameters

### -param randomAccessStream [in]

The source <a href="/previous-versions/hh438400(v=vs.85)">IRandomAccessStream</a>.

### -param riid [in]

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_IStream. This object encapsulates <i>randomAccessStream</i>.

### -param ppv [out]

When this method returns successfully, contains the interface pointer requested in <i>riid</i>, typically <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

We recommend that you use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args">IID_PPV_ARGS</a> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.

## -see-also

<a href="/windows/desktop/api/shcore/nf-shcore-createrandomaccessstreamonfile">CreateRandomAccessStreamOnFile</a>



<a href="/windows/desktop/api/shcore/nf-shcore-createrandomaccessstreamoverstream">CreateRandomAccessStreamOverStream</a>



<a href="/uwp/api/windows.storage.streams.randomaccessstream">RandomAccessStream</a>