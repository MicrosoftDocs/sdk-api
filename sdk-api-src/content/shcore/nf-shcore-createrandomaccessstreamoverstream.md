---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

