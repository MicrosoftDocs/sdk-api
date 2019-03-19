---
UID: NF:coml2api.GetHGlobalFromILockBytes
title: GetHGlobalFromILockBytes function (coml2api.h)
author: windows-sdk-content
description: The GetHGlobalFromILockBytes function retrieves a global memory handle to a byte array object created using the CreateILockBytesOnHGlobal function.
old-location: stg\gethglobalfromilockbytes.htm
tech.root: Stg
ms.assetid: 084fcd1d-5b85-448c-862a-378353e1e2e6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetHGlobalFromILockBytes, GetHGlobalFromILockBytes function [Structured Storage], _stg_gethglobalfromilockbytes, coml2api/GetHGlobalFromILockBytes, stg.gethglobalfromilockbytes
ms.topic: function
req.header: coml2api.h
req.include-header: Ole2.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
api_name:
 - GetHGlobalFromILockBytes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetHGlobalFromILockBytes function


## -description


The 
<b>GetHGlobalFromILockBytes</b> function retrieves a global memory handle to a byte array object created using the 
<a href="https://msdn.microsoft.com/e7963be7-ccd8-49fb-85bb-e22fbbb6dc5c">CreateILockBytesOnHGlobal</a> function.


## -parameters




### -param plkbyt [in]

Pointer to the 
<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> interface on the byte-array object previously created by a call to the 
<a href="https://msdn.microsoft.com/e7963be7-ccd8-49fb-85bb-e22fbbb6dc5c">CreateILockBytesOnHGlobal</a> function.


### -param phglobal [out]

Pointer to the current memory handle used by the specified byte-array object.


## -returns



This function returns HRESULT.




## -remarks



After a call to 
<a href="https://msdn.microsoft.com/e7963be7-ccd8-49fb-85bb-e22fbbb6dc5c">CreateILockBytesOnHGlobal</a>, which creates a byte array object on global memory, 
<b>GetHGlobalFromILockBytes</b> retrieves a pointer to the handle of the global memory underlying the byte array object. The handle this function returns might be different from the original handle due to intervening calls to the <a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a> function.

The contents of the returned memory handle can be written to a clean disk file, and then opened as a storage object using the 
<a href="https://msdn.microsoft.com/5ff18dc8-b24f-42bb-8c32-efc4d3696687">StgOpenStorage</a> function.

This function only works within the same process from which the byte array was created.




## -see-also




<a href="https://msdn.microsoft.com/e7963be7-ccd8-49fb-85bb-e22fbbb6dc5c">CreateILockBytesOnHGlobal</a>



<a href="https://msdn.microsoft.com/5ff18dc8-b24f-42bb-8c32-efc4d3696687">StgOpenStorage</a>
 

 

