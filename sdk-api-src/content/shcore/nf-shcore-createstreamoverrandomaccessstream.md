---
UID: NF:shcore.CreateStreamOverRandomAccessStream
title: CreateStreamOverRandomAccessStream function
author: windows-sdk-content
description: Creates an IStream around a Windows Runtime IRandomAccessStream object.
old-location: winrt\createstreamoverrandomaccessstream.htm
old-project: WinRT
ms.assetid: F9AB8A34-8AB1-4EF1-8659-DAD5713A89BF
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: CreateStreamOverRandomAccessStream, CreateStreamOverRandomAccessStream function [Windows Runtime], shcore/CreateStreamOverRandomAccessStream, winrt.createstreamoverrandomaccessstream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shcore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BSOS_OPTIONS
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
product: Windows
targetos: Windows
req.lib: ShCore.lib
req.dll: ShCore.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CreateStreamOverRandomAccessStream function


## -description


Creates an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> around a Windows Runtime <a href="https://msdn.microsoft.com/D2ECEB3D-D13E-44C1-BFE2-1AA57F7432C6">IRandomAccessStream</a> object.


## -parameters




### -param randomAccessStream [in]

The source <a href="https://msdn.microsoft.com/D2ECEB3D-D13E-44C1-BFE2-1AA57F7432C6">IRandomAccessStream</a>.


### -param riid [in]

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_IStream. This object encapsulates <i>randomAccessStream</i>.


### -param ppv [out]

When this method returns successfully, contains the interface pointer requested in <i>riid</i>, typically <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



We recommend that you use the <a href="https://msdn.microsoft.com/268B59FA-44EB-4777-8162-C50981CBDD09">IID_PPV_ARGS</a> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.




## -see-also




<a href="https://msdn.microsoft.com/6D3D2B25-7373-4BA5-BF6B-FB461C2DE982">CreateRandomAccessStreamOnFile</a>



<a href="https://msdn.microsoft.com/7A4BA702-0E2E-4FA9-8BEB-313D2D29762E">CreateRandomAccessStreamOverStream</a>



<a href="https://msdn.microsoft.com/dec8e90e-2cbb-497c-ad7f-c77c713af83c">RandomAccessStream</a>
 

 

