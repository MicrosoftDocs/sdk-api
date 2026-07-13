---
UID: NS:ws2spi._NSPV2_ROUTINE
title: NSPV2_ROUTINE (ws2spi.h)
description: Contains information on the functions implemented by a namespace service provider version-2 (NSPv2) provider.
helpviewer_keywords: ["*LPNSPV2_ROUTINE","*PNSPV2_ROUTINE","NSPV2_ROUTINE","NSPV2_ROUTINE structure [Winsock]","PNSPV2_ROUTINE","PNSPV2_ROUTINE structure pointer [Winsock]","winsock.nspv2_routine","ws2spi/NSPV2_ROUTINE","ws2spi/PNSPV2_ROUTINE"]
old-location: winsock\nspv2_routine.htm
tech.root: WinSock
ms.assetid: 22a4ee47-030b-4aee-b9b1-c9e33b3e4fce
ms.date: 12/05/2018
ms.keywords: '*LPNSPV2_ROUTINE, *PNSPV2_ROUTINE, NSPV2_ROUTINE, NSPV2_ROUTINE structure [Winsock], PNSPV2_ROUTINE, PNSPV2_ROUTINE structure pointer [Winsock], winsock.nspv2_routine, ws2spi/NSPV2_ROUTINE, ws2spi/PNSPV2_ROUTINE'
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: NSPV2_ROUTINE, *PNSPV2_ROUTINE, *LPNSPV2_ROUTINE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NSPV2_ROUTINE
 - ws2spi/_NSPV2_ROUTINE
 - PNSPV2_ROUTINE
 - ws2spi/PNSPV2_ROUTINE
 - NSPV2_ROUTINE
 - ws2spi/NSPV2_ROUTINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2spi.h
api_name:
 - NSPV2_ROUTINE
---

# NSPV2_ROUTINE structure


## -description

The **NSPV2_ROUTINE** structure contains information on the functions implemented by a namespace service provider version-2 (NSPv2) provider.<div class="alert">**Note**  The <i>Ws2spi.h</i> header file structure contains complete prototypes for all the NSPV2 function pointers.</div>
<div> </div>

## -struct-fields

### -field cbSize

Type: **DWORD**

The size, in bytes, of the structure.

### -field dwMajorVersion

Type: **DWORD**

The major version of the service provider specification supported by this provider.

### -field dwMinorVersion

Type: **DWORD**

The minor version of the service provider specification supported by this provider.

### -field NSPv2Startup

Type: **LPNSPV2STARTUP**

A pointer to the <a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2startup">NSPv2Startup</a> function for this NSPv2 provider.

### -field NSPv2Cleanup

Type: **LPNSPV2CLEANUP**

A pointer to the <a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2cleanup">NSPv2Cleanup</a> function for this NSPv2 provider.

### -field NSPv2LookupServiceBegin

Type: **LPNSPV2LOOKUPSERVICEBEGIN**

A pointer to the <a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPv2LookupServiceBegin</a> function for this NSPv2 provider.

### -field NSPv2LookupServiceNextEx

Type: **LPNSPV2LOOKUPSERVICENEXTEX**

A pointer to the <a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2lookupservicenextex">NSPv2LookupServiceNextEx</a> function for this NSPv2 provider.

### -field NSPv2LookupServiceEnd

Type: **LPNSPV2LOOKUPSERVICEEND**

A pointer to the <a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2lookupserviceend">NSPv2LookupServiceEnd</a> function for this NSPv2 provider.

### -field NSPv2SetServiceEx

Type: **LPNSPV2SETSERVICEEX**

A pointer to the <a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2setserviceex">NSPv2SetServiceEx</a> function for this NSPv2 provider.

### -field NSPv2ClientSessionRundown

Type: **LPNSPV2CLIENTSESSIONRUNDOWN**

A pointer to the <a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2clientsessionrundown">NSPv2ClientSessionRundown</a> function for this NSPv2 provider.

## -remarks

The 
**NSPV2_ROUTINE** structure is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the **NSPV2_ROUTINE** structure can only be used for operations on NS_EMAIL namespace providers.

The 
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaadvertiseprovider">WSAAdvertiseProvider</a> function advertises an instance of a NSPv2 provider for clients to find. The **WSAAdvertiseProvider** caller passes a pointer to an **NSPV2_ROUTINE**  structure in the <i>pNSPv2Routine</i> parameter with the NSPv2 entry points supported by the provider. 


A NSPv2 provider is required to implement the following functions: 
- 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPv2LookupServiceBegin</a>
 
- 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2lookupservicenextex">NSPv2LookupServiceNextEx</a>
 
- 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2lookupserviceend">NSPv2LookupServiceEnd</a>
 
 All other functions are optional, dependent on the requirements of the NSPv2 provider. 

 If a function isn't implemented, then calls to that function should be intercepted by a stub function that returns <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP">WSAEOPNOTSUPP</a>.  The NSPv2 function pointer to the unimplemented function in the **NSPV2_ROUTINE** structure should point be to the stub function. 

In general, NSPv2 providers are implemented in processes other than the calling applications. NSPv2 providers are not activated as a result of client activity. Each provider hosting application decides when to make a specific provider available or unavailable by calling the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaadvertiseprovider">WSAAdvertiseProvider</a> and <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaunadvertiseprovider">WSAUnadvertiseProvider</a> functions. The client activity only results in attempts to contact the provider, when available (when the namespace provider is advertised).

A process can implement and advertise multiple providers at the same time. Windows Sockets will manage the namespace providers by dispatching calls to the correct one. It will also hide RPC interface details and translates cross-process calls into in-process calls. So that the NSPv2 provider has only to implement a table of entry point functions similar to the <a href="/windows/desktop/api/ws2spi/ns-ws2spi-nsp_routine">NSP_ROUTINE</a> structure used by an NSPv1 provider. A NSPv2 provider does not have to worry about RPC specific requirements (data marshalling and serialization, for example).



The 
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaunadvertiseprovider">WSAUnadvertiseProvider</a> function makes a specific namespace provider no longer available for clients.

## -see-also

<a href="/windows/desktop/api/ws2spi/ns-ws2spi-nsp_routine">NSP_ROUTINE</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2cleanup">NSPv2Cleanup</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2clientsessionrundown">NSPv2ClientSessionRundown</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPv2LookupServiceBegin</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2lookupserviceend">NSPv2LookupServiceEnd</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2lookupservicenextex">NSPv2LookupServiceNextEx</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2setserviceex">NSPv2SetServiceEx</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2startup">NSPv2Startup</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaadvertiseprovider">WSAAdvertiseProvider</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaprovidercompleteasynccall">WSAProviderCompleteAsyncCall</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaqueryset2w">WSAQUERYSET2</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaunadvertiseprovider">WSAUnadvertiseProvider</a>

