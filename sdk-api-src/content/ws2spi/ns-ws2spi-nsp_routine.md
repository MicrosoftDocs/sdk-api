---
UID: NS:ws2spi._NSP_ROUTINE
title: NSP_ROUTINE
author: windows-sdk-content
description: Contains information regarding the functions implemented by a namespace service provider version 1 (NSPv1) provider.
old-location: winsock\nsp_routine.htm
tech.root: WinSock
ms.assetid: 8f7736d5-ea77-472a-a94f-e422398fae3f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPNSP_ROUTINE, NSP_ROUTINE, NSP_ROUTINE structure [Winsock], NSP_ROUTINE,FAR * LPNSP_ROUTINE, NSP_ROUTINE,FAR * LPNSP_ROUTINE structure [Winsock], winsock.nsp_routine, ws2spi/NSP_ROUTINE"
ms.topic: struct
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2spi.h
api_name:
 - NSP_ROUTINE, FAR * LPNSP_ROUTINE
product: Windows
targetos: Windows
req.typenames: NSP_ROUTINE, *LPNSP_ROUTINE
req.redist: 
---

# NSP_ROUTINE structure


## -description


The <b>NSP_ROUTINE</b> structure contains information regarding the functions implemented by a namespace service provider version 1 (NSPv1) provider.
<div class="alert"><b>Note</b>  The <i>Ws2spi.h</i> header file structure contains complete prototypes for all the NSPv1 function pointers.</div><div> </div>

## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size, in bytes, of the structure. Note that the size of the <b>NSP_ROUTINE</b> structure changed on Windows XP and later.


### -field dwMajorVersion

Type: <b>DWORD</b>

The major version of the service provider specification supported by this provider.


### -field dwMinorVersion

Type: <b>DWORD</b>

The minor version of the service provider specification supported by this provider.


### -field NSPCleanup

Type: <b>LPNSPCLEANUP</b>

A pointer to the <a href="https://msdn.microsoft.com/bef888a2-7cfd-4096-bd03-e1864af42365">NSPCleanup</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPCleanup</b> function should return <a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a>.


### -field NSPLookupServiceBegin

Type: <b>LPNSPLOOKUPSERVICEBEGIN</b>

A pointer to the <a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPLookupServiceBegin</b> function should return <a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a>.


### -field NSPLookupServiceNext

Type: <b>LPNSPLOOKUPSERVICENEXT</b>

A pointer to the <a href="https://msdn.microsoft.com/321732e4-5d48-48f4-8795-ffac208852dc">NSPLookupServiceNext</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPLookupServiceNext</b> function should return <a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a>. 



							


### -field NSPLookupServiceEnd

Type: <b>LPNSPLOOKUPSERVICEEND</b>

A pointer to the <a href="https://msdn.microsoft.com/ec72c89a-a74b-449c-996a-02057dff9137">NSPLookupServiceEnd</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPLookupServiceEnd</b> function should return <a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a>.


### -field NSPSetService

Type: <b>LPNSPSETSERVICE</b>

A pointer to the <a href="https://msdn.microsoft.com/df76ea75-c0bc-48b8-b1a7-0c510c5cc28d">NSPSetService</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPSetService</b> function should return <a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a>.


### -field NSPInstallServiceClass

Type: <b>LPNSPINSTALLSERVICECLASS</b>

A pointer to the <a href="https://msdn.microsoft.com/437a3580-e296-4f20-8921-84e522cccc1a">NSPInstallServiceClass</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPInstallServiceClass</b> function should return <a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a>. 



							


### -field NSPRemoveServiceClass

Type: <b>LPNSPREMOVESERVICECLASS</b>

A pointer to the <a href="https://msdn.microsoft.com/97313e6f-ec9e-4dcb-b888-14436259a519">NSPRemoveServiceClass</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPRemoveServiceClass</b> function should return <a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a>. 



							


### -field NSPGetServiceClassInfo

Type: <b>LPNSPGETSERVICECLASSINFO</b>

A pointer to the <a href="https://msdn.microsoft.com/babe1c96-9077-4d91-a52a-839c89d7a83b">NSPGetServiceClassInfo</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPGetServiceClassInfo</b> function should return <a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a>. 



							


### -field NSPIoctl

Type: <b>LPNSPIOCTL</b>

A pointer to the <a href="https://msdn.microsoft.com/061969f5-dbb5-47d7-820d-5af6fe6a0c62">NSPIoctl</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPIoctl</b> function should return <a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a>.

<div class="alert"><b>Note</b>  This structure member is only available on Windows XP and later.
</div>
<div> </div>

## -remarks



The size of the <b>NSP_ROUTINE</b> structure changed on Windows XP and later. The <b>cbSize</b> member should be used to determine which version of the <b>NSP_ROUTINE</b> structure is being used. 



The version of the <b>NSP_ROUTINE</b> structure on Windows XP and later has the following new member added: <b>NSPIoctl</b>.






## -see-also




<a href="https://msdn.microsoft.com/bef888a2-7cfd-4096-bd03-e1864af42365">NSPCleanup</a>



<a href="https://msdn.microsoft.com/babe1c96-9077-4d91-a52a-839c89d7a83b">NSPGetServiceClassInfo</a>



<a href="https://msdn.microsoft.com/437a3580-e296-4f20-8921-84e522cccc1a">NSPInstallServiceClass</a>



<a href="https://msdn.microsoft.com/061969f5-dbb5-47d7-820d-5af6fe6a0c62">NSPIoctl</a>



<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a>



<a href="https://msdn.microsoft.com/ec72c89a-a74b-449c-996a-02057dff9137">NSPLookupServiceEnd</a>



<a href="https://msdn.microsoft.com/321732e4-5d48-48f4-8795-ffac208852dc">NSPLookupServiceNext</a>



<a href="https://msdn.microsoft.com/97313e6f-ec9e-4dcb-b888-14436259a519">NSPRemoveServiceClass</a>



<a href="https://msdn.microsoft.com/df76ea75-c0bc-48b8-b1a7-0c510c5cc28d">NSPSetService</a>



<a href="https://msdn.microsoft.com/ed9e4ff3-736a-4037-bf85-5572f0cd279d">NSPStartup</a>



<a href="https://msdn.microsoft.com/22a4ee47-030b-4aee-b9b1-c9e33b3e4fce">NSPV2_ROUTINE</a>
 

 

