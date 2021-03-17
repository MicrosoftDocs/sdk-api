---
UID: NF:iphlpapi.NhpAllocateAndGetInterfaceInfoFromStack
title: NhpAllocateAndGetInterfaceInfoFromStack function (iphlpapi.h)
description: The NhpAllocateAndGetInterfaceInfoFromStack function obtains adapter information about the local computer.
helpviewer_keywords: ["NhpAllocateAndGetInterfaceInfoFromStack","NhpAllocateAndGetInterfaceInfoFromStack function [IP Helper]","iphlp.nhpallocateandgetinterfaceinfofromstack","iphlpapi/NhpAllocateAndGetInterfaceInfoFromStack"]
old-location: iphlp\nhpallocateandgetinterfaceinfofromstack.htm
tech.root: IpHlp
ms.assetid: a5ba8b28-4c15-4646-91d0-b6ef9e0f1e89
ms.date: 12/05/2018
ms.keywords: NhpAllocateAndGetInterfaceInfoFromStack, NhpAllocateAndGetInterfaceInfoFromStack function [IP Helper], iphlp.nhpallocateandgetinterfaceinfofromstack, iphlpapi/NhpAllocateAndGetInterfaceInfoFromStack
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NhpAllocateAndGetInterfaceInfoFromStack
 - iphlpapi/NhpAllocateAndGetInterfaceInfoFromStack
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - NhpAllocateAndGetInterfaceInfoFromStack
---

# NhpAllocateAndGetInterfaceInfoFromStack function


## -description

<p class="CCE_Message">[This function is no longer available for use as of Windows Vista. Instead, use the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a>  function and the associated <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a> structure.]

The <b>NhpAllocateAndGetInterfaceInfoFromStack</b> function obtains adapter information about the local computer.

## -parameters

### -param ppTable

An array of <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_interface_name_info_w2ksp1">IP_INTERFACE_NAME_INFO</a> structures that contains information about each adapter on the local system. The array contains one element for each adapter on the system.

### -param pdwCount

The number of elements in the <i>ppTable</i> array.

### -param bOrder

When <b>TRUE</b>, elements in the <i>ppTable</i> array are sorted by increasing index value.

### -param hHeap

A handle that specifies the heap from which <i>ppTable</i> should be allocated. This parameter can be the process heap returned by a call to the <a href="/windows/desktop/api/heapapi/nf-heapapi-getprocessheap">GetProcessHeap</a> function, or a private heap created by a call to the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a> function.

### -param dwFlags

A set of flags to be passed to the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> function when allocating memory for <i>ppTable</i>. See the <b>HeapAlloc</b> function for more information.

## -returns

Returns ERROR_SUCCESS upon successful completion.

## -remarks

In the Microsoft Windows Software Development Kit (SDK), the <b>NhpAllocateAndGetInterfaceInfoFromStack</b> function is  defined on Windows 2000 with Service Pack 1 (SP1) and later. When compiling an application, if the target platform is Windows 2000 with SP1 and later (<code>NTDDI_VERSION &gt;= NTDDI_WIN2KSP1</code>, <code>_WIN32_WINNT &gt;= 0x0500</code>, or <code>WINVER &gt;= 0x0500</code>), the <b>NhpAllocateAndGetInterfaceInfoFromStack</b> is defined.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-getprocessheap">GetProcessHeap</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP
				Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP
				Helper Start Page</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_interface_name_info_w2ksp1">IP_INTERFACE_NAME_INFO</a>