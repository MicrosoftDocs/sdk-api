---
UID: NF:lmaccess.NetGetAnyDCName
title: NetGetAnyDCName function (lmaccess.h)
description: The NetGetAnyDCName function returns the name of any domain controller (DC) for a domain that is directly trusted by the specified server.
helpviewer_keywords: ["NetGetAnyDCName","NetGetAnyDCName function [Network Management]","_win32_netgetanydcname","lmaccess/NetGetAnyDCName","netmgmt.netgetanydcname"]
old-location: netmgmt\netgetanydcname.htm
tech.root: NetMgmt
ms.assetid: 64dacbf4-46c2-4f82-b250-b7d338535e7c
ms.date: 12/05/2018
ms.keywords: NetGetAnyDCName, NetGetAnyDCName function [Network Management], _win32_netgetanydcname, lmaccess/NetGetAnyDCName, netmgmt.netgetanydcname
req.header: lmaccess.h
req.include-header: Lm.h
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetGetAnyDCName
 - lmaccess/NetGetAnyDCName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetGetAnyDCName
---

# NetGetAnyDCName function


## -description

The
				<b>NetGetAnyDCName</b> function returns the name of any domain controller (DC) for a domain that is directly trusted by the specified server.

Applications that support DNS-style names should call the 
<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> function. This function can locate any DC in any domain, whether or not the domain is directly trusted by the specified server.

## -parameters

### -param servername [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. For more information, see the following Remarks section.

### -param domainname [in]

Pointer to a constant string that specifies the name of the domain. If this parameter is <b>NULL</b>, the name of the domain controller for the primary domain is used. For more information, see the following Remarks section.

### -param bufptr [out]

Pointer to an allocated buffer that receives a string that specifies the server name of a domain controller for the domain. The server name is prefixed by \\. This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_LOGON_SERVERS</b></dt>
</dl>
</td>
<td width="60%">
No domain controllers could be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_DOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The specified domain is not a trusted domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_TRUST_LSA_SECRET</b></dt>
</dl>
</td>
<td width="60%">
The client side of the trust relationship is broken.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_TRUST_SAM_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
The server side of the trust relationship is broken or the password is broken.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DOMAIN_TRUST_INCONSISTENT</b></dt>
</dl>
</td>
<td width="60%">
The server that responded is not a proper domain controller of the specified domain.

</td>
</tr>
</table>

## -remarks

No special group membership is required to successfully execute the 
<b>NetGetAnyDCName</b> function.

If <i>servername</i> specifies a stand-alone workstation or a stand-alone server, no <i>domainname</i> is valid.

If <i>servername</i> specifies a workstation that is a member of a domain, or a server that is a member of a domain, the <i>domainname</i> must be in the same domain as <i>servername</i>.

If <i>servername</i> specifies a domain controller, the <i>domainname</i> must be one of the domains trusted by the domain for which the server is a controller. The domain controller that this call finds has been operational at least once during this call.

## -see-also

<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a>



<a href="/windows/desktop/NetMgmt/get-functions">Get Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgetdcname">NetGetDCName</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>