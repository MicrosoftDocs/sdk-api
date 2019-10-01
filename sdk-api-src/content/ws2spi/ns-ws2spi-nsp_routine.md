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

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspcleanup">NSPCleanup</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPCleanup</b> function should return <a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a>.


### -field NSPLookupServiceBegin

Type: <b>LPNSPLOOKUPSERVICEBEGIN</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPLookupServiceBegin</b> function should return <a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a>.


### -field NSPLookupServiceNext

Type: <b>LPNSPLOOKUPSERVICENEXT</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicenext">NSPLookupServiceNext</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPLookupServiceNext</b> function should return <a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a>. 



							


### -field NSPLookupServiceEnd

Type: <b>LPNSPLOOKUPSERVICEEND</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupserviceend">NSPLookupServiceEnd</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPLookupServiceEnd</b> function should return <a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a>.


### -field NSPSetService

Type: <b>LPNSPSETSERVICE</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspsetservice">NSPSetService</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPSetService</b> function should return <a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a>.


### -field NSPInstallServiceClass

Type: <b>LPNSPINSTALLSERVICECLASS</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspinstallserviceclass">NSPInstallServiceClass</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPInstallServiceClass</b> function should return <a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a>. 



							


### -field NSPRemoveServiceClass

Type: <b>LPNSPREMOVESERVICECLASS</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspremoveserviceclass">NSPRemoveServiceClass</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPRemoveServiceClass</b> function should return <a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a>. 



							


### -field NSPGetServiceClassInfo

Type: <b>LPNSPGETSERVICECLASSINFO</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspgetserviceclassinfo">NSPGetServiceClassInfo</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPGetServiceClassInfo</b> function should return <a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a>. 



							


### -field NSPIoctl

Type: <b>LPNSPIOCTL</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnspioctl">NSPIoctl</a> function implemented by the namespace provider. Every NSP function entry must point to a valid function. If the provider does not implement this function, the <b>NSPIoctl</b> function should return <a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a>.

<div class="alert"><b>Note</b>  This structure member is only available on Windows XP and later.
</div>
<div> </div>

## -remarks



The size of the <b>NSP_ROUTINE</b> structure changed on Windows XP and later. The <b>cbSize</b> member should be used to determine which version of the <b>NSP_ROUTINE</b> structure is being used. 



The version of the <b>NSP_ROUTINE</b> structure on Windows XP and later has the following new member added: <b>NSPIoctl</b>.






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
 

 

