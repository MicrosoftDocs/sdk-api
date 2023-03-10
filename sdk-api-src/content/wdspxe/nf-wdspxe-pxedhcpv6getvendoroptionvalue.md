---
UID: NF:wdspxe.PxeDhcpv6GetVendorOptionValue
title: PxeDhcpv6GetVendorOptionValue function (wdspxe.h)
description: Retrieves option values from the OPTION_VENDOR_OPTS (17) field of a DHCPv6 packet.
helpviewer_keywords: ["PxeDhcpv6GetVendorOptionValue","PxeDhcpv6GetVendorOptionValue function [Windows Deployment Services]","wds.pxedhcpv6getvendoroptionvalue","wdspxe/PxeDhcpv6GetVendorOptionValue"]
old-location: wds\pxedhcpv6getvendoroptionvalue.htm
tech.root: wds
ms.assetid: 9F969C0C-93CA-4355-8556-2F43542570F1
ms.date: 12/05/2018
ms.keywords: PxeDhcpv6GetVendorOptionValue, PxeDhcpv6GetVendorOptionValue function [Windows Deployment Services], wds.pxedhcpv6getvendoroptionvalue, wdspxe/PxeDhcpv6GetVendorOptionValue
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PxeDhcpv6GetVendorOptionValue
 - wdspxe/PxeDhcpv6GetVendorOptionValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsPxe.dll
api_name:
 - PxeDhcpv6GetVendorOptionValue
---

# PxeDhcpv6GetVendorOptionValue function


## -description

Retrieves option values from the OPTION_VENDOR_OPTS (17) field of a DHCPv6 
    packet.

## -parameters

### -param pPacket [in]

Pointer to a reply packet allocated with the 
      <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a> function.

### -param uPacketLen [in]

Length of the packet pointed to by the <i>pReplyPacket</i> parameter.

### -param dwEnterpriseNumber [in]

An Enterprise Number assigned to the vendor of the option by the Internet Assigned Numbers Authority (IANA).

For more information about assigned Enterprise Numbers, developers should refer to the Dynamic Host Configuration Protocol for IPv6 (<a href="https://www.ietf.org/rfc/rfc3315.txt">RFC 3315</a>) maintained by The Internet Engineering Task Force (IETF).

### -param wOption [in]

Option whose value will be retrieved.

### -param uInstance [in]

One-based index that specifies which instance of the <i>wOption</i> parameter to 
      retrieve.

### -param pwOptionLen [out, optional]

Address of <b>WORD</b> which will receive the length of the option value.

### -param ppOptionValue [out, optional]

Address of <b>PVOID</b> which will receive the address of the option value inside the 
      packet.

## -returns

Common return values are listed in the following table. For all other failures, an appropriate Windows 
      error code is returned.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
The option was found and a pointer to the value was returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
The option was not located.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
<dt>13 (0xD)</dt>
</dl>
</td>
<td width="60%">
The packet is not a valid DHCP packet. This test is not as thorough as the tests used by the 
        <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxedhcpv6isvalid">PxeDhcpv6IsValid</a> function; only the packet length and 
        magic cookie are verified.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxedhcpv6getoptionvalue">PxeDhcpv6GetOptionValue</a>



<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a>



<a href="/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>