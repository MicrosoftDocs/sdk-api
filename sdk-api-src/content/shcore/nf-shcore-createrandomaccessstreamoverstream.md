---
UID: NF:shcore.CreateRandomAccessStreamOverStream
title: CreateRandomAccessStreamOverStream function
author: windows-sdk-content
description: Creates a Windows Runtime random access stream around an IStream base implementation.
old-location: winrt\createrandomaccessstreamoverstream.htm
old-project: WinRT
ms.assetid: 7A4BA702-0E2E-4FA9-8BEB-313D2D29762E
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: CreateRandomAccessStreamOverStream, CreateRandomAccessStreamOverStream function [Windows Runtime], shcore/CreateRandomAccessStreamOverStream, winrt.createrandomaccessstreamoverstream
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
 - API-MS-Win-ShCore-Stream-WinRT-l1-1-0.dll
api_name:
 - CreateRandomAccessStreamOverStream
product: Windows
targetos: Windows
req.lib: ShCore.lib
req.dll: ShCore.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CreateRandomAccessStreamOverStream function


## -description


Creates a  Windows Runtime random access stream around an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> base implementation.


## -parameters




### -param stream [in]

The COM stream to encapsulate.


### -param options [in]

One of the <a href="https://msdn.microsoft.com/C51D945B-37C6-44CB-BF80-5FA62EE1F477">BSOS_OPTIONS</a> options that specify the behavior of the <a href="https://msdn.microsoft.com/dec8e90e-2cbb-497c-ad7f-c77c713af83c">RandomAccessStream</a> that encapsulates <i>stream</i>.


### -param riid [in]

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_RandomAccessStream.


### -param ppv [out]

When this method returns successfully, contains the interface pointer to the <a href="https://msdn.microsoft.com/dec8e90e-2cbb-497c-ad7f-c77c713af83c">RandomAccessStream</a> that encapsulates <i>stream</i> requested in <i>riid</i>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use the <b>CreateRandomAccessStreamOverStream</b> function to create a <a href="https://msdn.microsoft.com/dec8e90e-2cbb-497c-ad7f-c77c713af83c">RandomAccessStream</a> that encapsulates a COM <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>.

For info on utility classes that help with interoperation between Windows Runtime and COM streams, see the Remarks at <b>RandomAccessStreamOverStream</b>.

We recommend that you use the <a href="https://msdn.microsoft.com/268B59FA-44EB-4777-8162-C50981CBDD09">IID_PPV_ARGS</a> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.




## -see-also




<a href="https://msdn.microsoft.com/6D3D2B25-7373-4BA5-BF6B-FB461C2DE982">CreateRandomAccessStreamOnFile</a>



<a href="https://msdn.microsoft.com/F9AB8A34-8AB1-4EF1-8659-DAD5713A89BF">CreateStreamOverRandomAccessStream</a>



<a href="https://msdn.microsoft.com/dec8e90e-2cbb-497c-ad7f-c77c713af83c">RandomAccessStream</a>
 

 

