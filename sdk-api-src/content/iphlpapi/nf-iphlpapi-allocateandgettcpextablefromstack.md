---
UID: NF:iphlpapi.AllocateAndGetTcpExTableFromStack
title: AllocateAndGetTcpExTableFromStack function (iphlpapi.h)
description: Retrieves the TCP connection table and allocates memory from the local heap to store the table.
helpviewer_keywords: ["AF_INET","AF_INET6","AllocateAndGetTcpExTableFromStack","AllocateAndGetTcpExTableFromStack function [IP Helper]","iphlp.allocateandgettcpextablefromstack","iphlpapi/AllocateAndGetTcpExTableFromStack"]
old-location: iphlp\allocateandgettcpextablefromstack.htm
tech.root: IpHlp
ms.assetid: c79dd5ba-e80b-494f-80fa-efa10c021773
ms.date: 12/05/2018
ms.keywords: AF_INET, AF_INET6, AllocateAndGetTcpExTableFromStack, AllocateAndGetTcpExTableFromStack function [IP Helper], iphlp.allocateandgettcpextablefromstack, iphlpapi/AllocateAndGetTcpExTableFromStack
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - AllocateAndGetTcpExTableFromStack
 - iphlpapi/AllocateAndGetTcpExTableFromStack
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
 - AllocateAndGetTcpExTableFromStack
---

# AllocateAndGetTcpExTableFromStack function


## -description

<p class="CCE_Message">[This function is no longer available for use as of Windows Vista. Instead, use the 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcptable">GetTcpTable</a> or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedtcptable">GetExtendedTcpTable</a> function to retrieve the TCP connection table.]

The <b>AllocateAndGetTcpExTableFromStack</b> function retrieves the TCP connection table and allocates memory from the local heap to store the table.

## -parameters

### -param ppTcpTable [out]

Pointer to the address of the opaque data that contains the TCP connection table after the function returns.

### -param bOrder [in]

If true, the TCP connection entries in the table returned in <i>ppTcpTable</i> are sorted; if false, they are not.

### -param hHeap [in]

Handle to the heap from which the memory to store the table will be allocated.

### -param dwFlags [in]

One or more flags that indicate specific heap allocation control behaviors.

### -param dwFamily [in]

The family of the TCP addresses in the table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
</dl>
</td>
<td width="60%">
Retrieve IPv4 TCP addresses.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
</dl>
</td>
<td width="60%">
Retrieve IPv6 TCP addresses.

</td>
</tr>
</table>

## -returns

If the function succeeds, it returns ERROR_SUCCESS.

If the function fails, it returns a function from winerror.h.

## -remarks

In the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the function prototype for <b>AllocateAndGetTcpExTableFromStack</b> is still defined in the Iphlpapi.h header file for continued support on Windows Server 2003 and Windows XP.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-allocateandgetudpextablefromstack">AllocateAndGetUdpExTableFromStack</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedtcptable">GetExtendedTcpTable</a>



<b>GetTcpTable</b>