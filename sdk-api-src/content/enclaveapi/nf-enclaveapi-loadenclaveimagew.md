---
UID: NF:enclaveapi.LoadEnclaveImageW
title: LoadEnclaveImageW function
author: windows-sdk-content
description: Loads an image and all of its imports into an enclave.
old-location: base\loadenclaveimage.htm
tech.root: Memory
ms.assetid: BC3F3EB4-BB5E-40D6-B877-50694576FA1B
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: LoadEnclaveIUmageA, LoadEnclaveImage, LoadEnclaveImage function, LoadEnclaveImageW, base.loadenclaveimage, enclaveapi/LoadEnclaveIUmageA, enclaveapi/LoadEnclaveImage, enclaveapi/LoadEnclaveImageW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: enclaveapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadEnclaveImageW (Unicode) and LoadEnclaveIUmageA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vertdll.lib
req.dll: Vertdll.dll; Api-ms-win-core-enclave-l1-1-0.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Vertdll.dll
 - api-ms-win-core-enclave-l1-1-0.dll
api_name:
 - LoadEnclaveImage
 - LoadEnclaveIUmageA
 - LoadEnclaveImageW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LoadEnclaveImageW function


## -description


Loads an image and all of its imports into an enclave.


## -parameters




### -param lpEnclaveAddress [in]

The base address of the image into which to load the image.


### -param lpImageName [in]

A NULL-terminated string that contains the name of the image to load.


## -returns



<b>TRUE</b> if the function succeeds; otherwise <b>FALSE</b>.  To get extended error information, 
       call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<b>LoadEnclaveImage</b> is only supported enclaves that have  the <b>ENCLAVE_TYPE_VBS</b> enclave type.




## -see-also




<a href="https://msdn.microsoft.com/2193AE42-D9CC-4A9C-8676-7DE432ED58C3">CreateEnclave</a>



<a href="https://msdn.microsoft.com/6A711135-A522-40AE-965F-E1AF97D0076A">InitializeEnclave</a>
 

 

