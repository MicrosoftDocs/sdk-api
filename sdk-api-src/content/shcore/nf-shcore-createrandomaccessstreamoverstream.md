---
UID: NF:shcore.CreateRandomAccessStreamOverStream
title: CreateRandomAccessStreamOverStream function (shcore.h)
description: Creates a Windows Runtime random access stream around an IStream base implementation.
helpviewer_keywords: ["CreateRandomAccessStreamOverStream","CreateRandomAccessStreamOverStream function [Windows Runtime]","shcore/CreateRandomAccessStreamOverStream","winrt.createrandomaccessstreamoverstream"]
old-location: winrt\createrandomaccessstreamoverstream.htm
tech.root: WinRT
ms.assetid: 7A4BA702-0E2E-4FA9-8BEB-313D2D29762E
ms.date: 12/05/2018
ms.keywords: CreateRandomAccessStreamOverStream, CreateRandomAccessStreamOverStream function [Windows Runtime], shcore/CreateRandomAccessStreamOverStream, winrt.createrandomaccessstreamoverstream
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
 - CreateRandomAccessStreamOverStream
 - shcore/CreateRandomAccessStreamOverStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ShCore.dll
 - API-MS-Win-ShCore-Stream-WinRT-l1-1-0.dll
api_name:
 - CreateRandomAccessStreamOverStream
---

# CreateRandomAccessStreamOverStream function


## -description

Creates a  Windows Runtime random access stream around an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> base implementation.

## -parameters

### -param stream [in]

The COM stream to encapsulate.

### -param options [in]

One of the <a href="/windows/desktop/api/shcore/ne-shcore-bsos_options">BSOS_OPTIONS</a> options that specify the behavior of the <a href="/uwp/api/windows.storage.streams.randomaccessstream">RandomAccessStream</a> that encapsulates <i>stream</i>.

### -param riid [in]

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_RandomAccessStream.

### -param ppv [out]

When this method returns successfully, contains the interface pointer to the <a href="/uwp/api/windows.storage.streams.randomaccessstream">RandomAccessStream</a> that encapsulates <i>stream</i> requested in <i>riid</i>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Use the <b>CreateRandomAccessStreamOverStream</b> function to create a <a href="/uwp/api/windows.storage.streams.randomaccessstream">RandomAccessStream</a> that encapsulates a COM <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>.

For info on utility classes that help with interoperation between Windows Runtime and COM streams, see the Remarks at <b>RandomAccessStreamOverStream</b>.

We recommend that you use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args">IID_PPV_ARGS</a> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.

## -see-also

<a href="/windows/desktop/api/shcore/nf-shcore-createrandomaccessstreamonfile">CreateRandomAccessStreamOnFile</a>



<a href="/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream">CreateStreamOverRandomAccessStream</a>



<a href="/uwp/api/windows.storage.streams.randomaccessstream">RandomAccessStream</a>