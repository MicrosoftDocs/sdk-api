---
UID: NF:dsgetdc.DsGetDcNextW
title: DsGetDcNextW function
author: windows-driver-content
description: Retrieves the next domain controller in a domain controller enumeration operation.
old-location: ad\dsgetdcnext.htm
old-project: AD
ms.assetid: 2906772f-4391-411b-b0a9-5a20ebb6c0ee
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: DsGetDcNext, DsGetDcNext function [Active Directory], DsGetDcNextA, DsGetDcNextW, ad.dsgetdcnext, dsgetdc/DsGetDcNext, dsgetdc/DsGetDcNextA, dsgetdc/DsGetDcNextW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dsgetdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsGetDcNextW (Unicode) and DsGetDcNextA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DSDISPLAYSPECOPTIONS, *PDSDISPLAYSPECOPTIONS, *LPDSDISPLAYSPECOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Netapi32.dll
api_name:
-	DsGetDcNext
-	DsGetDcNextA
-	DsGetDcNextW
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
---

# DsGetDcNextW function


## -description


The <b>DsGetDcNext</b> function retrieves the next domain controller in a domain controller enumeration operation.


## -parameters




### -param GetDcContextHandle [in]

Contains the domain controller enumeration context handle provided by the <a href="https://msdn.microsoft.com/2811cc30-f367-4f1a-8f0c-ed0a77dad24c">DsGetDcOpen</a> function.


### -param OPTIONAL

TBD




#### - DnsHostName [out, optional]

Pointer to a string pointer that receives the DNS name of the domain controller.
        This parameter receives <b>NULL</b> if no host name is known. The caller must free this memory when it is no longer required by calling <a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a>.


#### - SockAddressCount [out, optional]

Pointer to a <b>ULONG</b> value that receives the number of elements in the <i>SockAddresses</i> array.
        If this parameter is <b>NULL</b>, socket addresses are not retrieved.


#### - SockAddresses [out, optional]

Pointer to an array of <a href="https://msdn.microsoft.com/37fbcb96-a859-4eca-8928-8051f95407b9">SOCKET_ADDRESS</a> structures that receives the socket address data for the domain controller. <i>SockAddressCount</i> receives the number of elements in this array.

All returned addresses will be of type <b>AF_INET</b> or <b>AF_INET6</b>.
        The <b>sin_port</b> member contains the port from the server record.
            A port of 0 indicates no port is available from DNS.

The caller must free this memory when it is no longer required by calling <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>.

This parameter is ignored if <i>SockAddressCount</i> is <b>NULL</b>.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful or a Win32 or RPC error otherwise. Possible error values include the following.




## -remarks



To reset the enumeration, close the current enumeration by calling <a href="https://msdn.microsoft.com/d193e4cd-ad66-4d93-b912-348f17e93a6f">DsGetDcClose</a> and then reopen the enumeration by calling <a href="https://msdn.microsoft.com/2811cc30-f367-4f1a-8f0c-ed0a77dad24c">DsGetDcOpen</a> again.

The DC returned by <b>DsGetDcNext</b> will not be a Read-only DC (RODC) because those DCs only register site-specific and CName records, and both <b>DsGetDcNext</b> and <a href="https://msdn.microsoft.com/2811cc30-f367-4f1a-8f0c-ed0a77dad24c">DsGetDcOpen</a> look for DNS SRV records.

The following procedure shows how to get a complete DC list from a computer running Windows Server 2008.

<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To obtain a complete list of domain controllers</b>

<ol>
<li>Use <a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a> to get a domain controller name.</li>
<li>Use <a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a> to connect to that domain controller.</li>
<li>Call <a href="https://msdn.microsoft.com/52db3b25-e6b0-4a0d-831b-89a203580cf1">DsGetDomainControllerInfo</a> with InfoLevel 3 (<b>DS_DOMAIN_CONTROLLER_INFO_3</b>) to get the complete list, including RODCs.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/7b519c81-5a6c-470a-a525-1894efd53305">Directory Service Functions</a>



<a href="https://msdn.microsoft.com/d193e4cd-ad66-4d93-b912-348f17e93a6f">DsGetDcClose</a>



<a href="https://msdn.microsoft.com/2811cc30-f367-4f1a-8f0c-ed0a77dad24c">DsGetDcOpen</a>



<a href="https://msdn.microsoft.com/bfc92777-6944-406a-8b93-949a1cf3e2c3">Enumerating Domain Controllers</a>



<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>



<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a>



<a href="https://msdn.microsoft.com/37fbcb96-a859-4eca-8928-8051f95407b9">SOCKET_ADDRESS</a>
 

 

