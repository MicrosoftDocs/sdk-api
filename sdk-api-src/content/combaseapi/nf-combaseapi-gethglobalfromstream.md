---
UID: NF:combaseapi.GetHGlobalFromStream
title: GetHGlobalFromStream function (combaseapi.h)
description: The GetHGlobalFromStream function retrieves the global memory handle to a stream that was created through a call to the CreateStreamOnHGlobal function.
helpviewer_keywords: ["GetHGlobalFromStream","GetHGlobalFromStream function [Structured Storage]","_stg_gethglobalfromstream","combaseapi/GetHGlobalFromStream","stg.gethglobalfromstream"]
old-location: stg\gethglobalfromstream.htm
tech.root: Stg
ms.assetid: 79e39345-7a20-4b0f-bceb-f62de13d3260
ms.date: 12/05/2018
ms.keywords: GetHGlobalFromStream, GetHGlobalFromStream function [Structured Storage], _stg_gethglobalfromstream, combaseapi/GetHGlobalFromStream, stg.gethglobalfromstream
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetHGlobalFromStream
 - combaseapi/GetHGlobalFromStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - GetHGlobalFromStream
---

# GetHGlobalFromStream function


## -description

The <b>GetHGlobalFromStream</b> function retrieves the global memory handle to a stream that was created through a call to the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal">CreateStreamOnHGlobal</a> function.

## -parameters

### -param pstm [in]

<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> pointer to the stream object previously created by a call to the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal">CreateStreamOnHGlobal</a> function.

### -param phglobal [out]

Pointer to the current memory handle used by the specified stream object.

## -returns

This function returns HRESULT.

## -remarks

The handle <b>GetHGlobalFromStream</b> returns may be different from the original handle due to intervening <a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> calls.

This function can be called only from within the same process from which the byte array was created.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal">CreateStreamOnHGlobal</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a>