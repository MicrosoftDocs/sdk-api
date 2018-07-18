---
UID: NF:combaseapi.GetHGlobalFromStream
title: GetHGlobalFromStream function
author: windows-sdk-content
description: The GetHGlobalFromStream function retrieves the global memory handle to a stream that was created through a call to the CreateStreamOnHGlobal function.
old-location: stg\gethglobalfromstream.htm
old-project: stg
ms.assetid: 79e39345-7a20-4b0f-bceb-f62de13d3260
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: GetHGlobalFromStream, GetHGlobalFromStream function [Structured Storage], _stg_gethglobalfromstream, combaseapi/GetHGlobalFromStream, stg.gethglobalfromstream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: combaseapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: REGCLS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - GetHGlobalFromStream
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# GetHGlobalFromStream function


## -description


The <b>GetHGlobalFromStream</b> function retrieves the global memory handle to a stream that was created through a call to the 
<a href="https://msdn.microsoft.com/413c107b-a943-4c02-9c00-aea708e876d7">CreateStreamOnHGlobal</a> function.


## -parameters




### -param pstm [in]


<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> pointer to the stream object previously created by a call to the 
<a href="https://msdn.microsoft.com/413c107b-a943-4c02-9c00-aea708e876d7">CreateStreamOnHGlobal</a> function.


### -param phglobal [out]

Pointer to the current memory handle used by the specified stream object.


## -returns



This function returns HRESULT.




## -remarks



The handle <b>GetHGlobalFromStream</b> returns may be different from the original handle due to intervening <a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a> calls.

This function can be called only from within the same process from which the byte array was created.




## -see-also




<a href="https://msdn.microsoft.com/413c107b-a943-4c02-9c00-aea708e876d7">CreateStreamOnHGlobal</a>



<a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a>
 

 

