---
UID: NS:ws2spi._NSP_ROUTINE
title: NSP_ROUTINE (ws2spi.h)
author: windows-sdk-content
description: Contains information regarding the functions implemented by a namespace service provider version 1 (NSPv1) provider.
old-location: winsock\nsp_routine.htm
tech.root: WinSock
ms.assetid: 8f7736d5-ea77-472a-a94f-e422398fae3f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*LPNSP_ROUTINE, NSP_ROUTINE, NSP_ROUTINE structure [Winsock], NSP_ROUTINE,FAR * LPNSP_ROUTINE, NSP_ROUTINE,FAR * LPNSP_ROUTINE structure [Winsock], winsock.nsp_routine, ws2spi/NSP_ROUTINE'
ms.topic: struct
f1_keywords:
- ws2spi/NSP_ROUTINE, FAR * LPNSP_ROUTINE
dev_langs:
 - c++
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
targetos: Windows
req.typenames: NSP_ROUTINE, *LPNSP_ROUTINE
req.redist: 
ms.custom: 19H1
---

# NSP_ROUTINE structure


## -description


The **NSP_ROUTINE** structure contains information regarding the functions implemented by a namespace service provider version 1 (NSPv1) provider.
<div class="alert">**Note**  The <i>Ws2spi.h</i> header file structure contains complete prototypes for all the NSPv1 function pointers.</div><div> </div>

## -struct-fields




### -field cbSize

Type: **DWORD**

The size, in bytes, of the structure. Note that the size of the **NSP_ROUTINE** structure changed on Windows XP and later.


### -field dwMajorVersion

Type: **DWORD**

The major version of the service provider specification supported by this provider.


### -field dwMinorVersion

Type: **DWORD**

The minor version of the service provider specification supported by this provider.


### -field NSPCleanup

Type: **LPNSPCLEANUP**

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspcleanup">NSPCleanup</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the **NSPCleanup** function should return [WSAEOPNOTSUPP](https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP).


### -field NSPLookupServiceBegin

Type: **LPNSPLOOKUPSERVICEBEGIN**

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the **NSPLookupServiceBegin** function should return [WSAEOPNOTSUPP](https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP).


### -field NSPLookupServiceNext

Type: **LPNSPLOOKUPSERVICENEXT**

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicenext">NSPLookupServiceNext</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the **NSPLookupServiceNext** function should return [WSAEOPNOTSUPP](https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP). 



							


### -field NSPLookupServiceEnd

Type: **LPNSPLOOKUPSERVICEEND**

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupserviceend">NSPLookupServiceEnd</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the **NSPLookupServiceEnd** function should return [WSAEOPNOTSUPP](https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP).


### -field NSPSetService

Type: **LPNSPSETSERVICE**

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspsetservice">NSPSetService</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the **NSPSetService** function should return [WSAEOPNOTSUPP](https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP).


### -field NSPInstallServiceClass

Type: **LPNSPINSTALLSERVICECLASS**

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspinstallserviceclass">NSPInstallServiceClass</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the **NSPInstallServiceClass** function should return [WSAEOPNOTSUPP](https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP). 



							


### -field NSPRemoveServiceClass

Type: **LPNSPREMOVESERVICECLASS**

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspremoveserviceclass">NSPRemoveServiceClass</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the **NSPRemoveServiceClass** function should return [WSAEOPNOTSUPP](https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP). 



							


### -field NSPGetServiceClassInfo

Type: **LPNSPGETSERVICECLASSINFO**

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspgetserviceclassinfo">NSPGetServiceClassInfo</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the **NSPGetServiceClassInfo** function should return [WSAEOPNOTSUPP](https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP). 



							


### -field NSPIoctl

Type: **LPNSPIOCTL**

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspioctl">NSPIoctl</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the **NSPIoctl** function should return [WSAEOPNOTSUPP](https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP).

<div class="alert">**Note**  This structure member is only available on Windows XP and later.
</div>
<div> </div>

## -remarks



The size of the **NSP_ROUTINE** structure changed on Windows XP and later. The **cbSize** member should be used to determine which version of the **NSP_ROUTINE** structure is being used. 



The version of the **NSP_ROUTINE** structure on Windows XP and later has the following new member added: **NSPIoctl**.






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspcleanup">NSPCleanup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspgetserviceclassinfo">NSPGetServiceClassInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspinstallserviceclass">NSPInstallServiceClass</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspioctl">NSPIoctl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupserviceend">NSPLookupServiceEnd</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicenext">NSPLookupServiceNext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspremoveserviceclass">NSPRemoveServiceClass</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspsetservice">NSPSetService</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-nspstartup">NSPStartup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/ns-ws2spi-nspv2_routine">NSPV2_ROUTINE</a>
 

 

