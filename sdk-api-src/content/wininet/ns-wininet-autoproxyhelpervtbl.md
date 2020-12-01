---
UID: NS:wininet.AutoProxyHelperVtbl
title: AutoProxyHelperVtbl (wininet.h)
description: The AutoProxyHelperVtbl structure creates a v-table of pointers to Proxy AutoConfig (PAC) helper functions.See the Navigator Proxy Auto-Config (PAC) File Format documentation for a specification of the form and use of Proxy Auto-Config helper functions.
helpviewer_keywords: ["AutoProxyHelperVtbl","AutoProxyHelperVtbl structure [WinINet]","wininet.autoproxyhelpervtbl","wininet/AutoProxyHelperVtbl"]
old-location: wininet\autoproxyhelpervtbl.htm
tech.root: wininet
ms.assetid: df482b8d-38e1-4d0d-a12c-8ba0f2e6423a
ms.date: 12/05/2018
ms.keywords: AutoProxyHelperVtbl, AutoProxyHelperVtbl structure [WinINet], wininet.autoproxyhelpervtbl, wininet/AutoProxyHelperVtbl
req.header: wininet.h
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
targetos: Windows
req.typenames: AutoProxyHelperVtbl
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AutoProxyHelperVtbl
 - wininet/AutoProxyHelperVtbl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - AutoProxyHelperVtbl
---

# AutoProxyHelperVtbl structure


## -description

The <b>AutoProxyHelperVtbl</b> structure creates a v-table of pointers to Proxy AutoConfig (PAC) helper functions.

See the   <a href="https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html">Navigator Proxy Auto-Config (PAC) File Format</a> documentation for a specification of the form and use of Proxy Auto-Config helper functions.

## -struct-fields

### -field IsResolvable

Tries to resolve a specified host name. This PAC function is described in the specification under the same name. Returns <b>TRUE</b> if the host name can be resolved, or <b>FALSE</b> otherwise.



#### lpszHost

Pointer to a string that contains the host name.

### -field GetIPAddress

Places the IP address of the local machine in a specified buffer. This PAC functions is described in the specification under the name <b>myIPAddress</b>. Returns zero if successful, or an error code if not.



#### lpszIPAddress

Pointer to a buffer in which the IP address is to be returned.



#### lpdwIPAddressSize

Size of the buffer pointed to by <b>lpszIPAddress</b>.

### -field ResolveHostName

Places an IP address that corresponds to a host-name string in a specified buffer. This PAC function is described in the specification under the name, <b>dnsResolve</b>. Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.



#### lpszHostName

Pointer to the host name to resolve.



#### lpszIPAddress

Pointer to a buffer in which the IP address is to be returned.



#### lpdwIPAddressSize

Size of the buffer pointed to by <b>lpszIPAddress</b>.

### -field IsInNet

Determines whether a specified IP address masked by a specified mask value matches a specified destination address. This PAC function is described in the specification under the same name. 

The comparison is performed by converting the string representations to binary, logically ANDing the mask and the address specified in <i>lpszIPAddress</i>, and comparing the result with the address specified in <i>lpszDest</i>.



#### lpszIPAddress

Pointer to a string representation of the IP address to mask; corresponds to the <i>host</i> parameter in the specification.



#### lpszDest

Pointer to a string representation of the IP address against which to compare; corresponds to the <i>pattern</i> parameter in the specification.



#### lpszMask

Pointer to a string representation of the mask to apply against the address pointed to by <i>lpszIPAddress</i>.

### -field IsResolvableEx

Tries to resolve a specified host name. This PAC function is described in the specification under the same name. Returns <b>TRUE</b> if the host name can be resolved, or <b>FALSE</b> otherwise.

<b>Windows XP and earlier:  </b>Available only in Windows XP with SP2 with Internet Explorer 7. Otherwise, not available.



#### lpszHost

String that contains the host name.

### -field GetIPAddressEx

Places the IP address of the local machine in a specified buffer. This PAC functions is described in the specification under the name <b>myIPAddress</b>. Returns zero if successful, or an error code if not.

<b>Windows XP and earlier:  </b>Available only in Windows XP with SP2 with Internet Explorer 7. Otherwise, not available.



#### lpszIPAddress

Pointer to a buffer in which the IP address is to be returned. 



#### lpdwIPAddressSize

The size of the buffer pointed to by <i>lpszIPAddress</i>.

### -field ResolveHostNameEx

Places an IP address that corresponds to a host-name string in a specified buffer. This PAC function is described in the specification under the name, <b>dnsResolve</b>. Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.

<b>Windows XP and earlier:  </b>Available only in Windows XP with SP2 with Internet Explorer 7. Otherwise, not available.



#### lpszHostName

Pointer to the host name to resolve.



#### lpszIPAddress

Pointer to a buffer in which the IP address is to be returned.



#### lpdwIPAddressSize

Size of the buffer pointed to by <i>lpszIPAddress</i>.

### -field IsInNetEx

Determines whether a specified IP address masked by a specified mask value matches a specified destination address. This PAC function is described in the specification under the same name. 

<b>Windows XP and earlier:  </b>Available only in Windows XP with SP2 with Internet Explorer 7. Otherwise, not available.



#### lpszIPAddress

Pointer to a string representation of the IP address to mask; corresponds to the <i>host</i> parameter in the specification.



#### lpszIPPrefix

Pointer so a string containing the IP address prefix.

### -field SortIpList

Sorts a list of IP addresses. 


<b>Windows XP and earlier:  </b>Available only in Windows XP with SP2 with Internet Explorer 7. Otherwise, not available.





#### lpszIPAddressList

Pointer to the list to sort.



#### lpszIPSortedList

Pointer to the sorted list.



#### lpdwIPSortedListSize

Pointer to a buffer containing the size of the sorted list.

## -remarks

Together with the <a href="/windows/desktop/api/wininet/ns-wininet-autoproxyhelperfunctions">AutoProxyHelperFunctions</a> structure, <b>AutoProxyHelperVtbl</b> serves to create a standard v-table that can be declared and populated using C, without requiring the use of C++.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wininet/ns-wininet-autoproxyhelperfunctions">AutoProxyHelperFunctions</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetinitializeautoproxydll">InternetInitializeAutoProxyDll</a>