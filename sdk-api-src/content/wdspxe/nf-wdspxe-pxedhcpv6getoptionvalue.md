---
UID: NF:wdspxe.PxeDhcpv6GetOptionValue
title: PxeDhcpv6GetOptionValue function (wdspxe.h)
description: Retrieves an option value from a DHCPv6 packet.
helpviewer_keywords: ["PxeDhcpv6GetOptionValue","PxeDhcpv6GetOptionValue function [Windows Deployment Services]","wds.pxedhcpv6getoptionvalue","wdspxe/PxeDhcpv6GetOptionValue"]
old-location: wds\pxedhcpv6getoptionvalue.htm
tech.root: wds
ms.assetid: 0DC0CF7F-0C74-4595-9DC6-9468E1E7DA20
ms.date: 12/05/2018
ms.keywords: PxeDhcpv6GetOptionValue, PxeDhcpv6GetOptionValue function [Windows Deployment Services], wds.pxedhcpv6getoptionvalue, wdspxe/PxeDhcpv6GetOptionValue
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
 - PxeDhcpv6GetOptionValue
 - wdspxe/PxeDhcpv6GetOptionValue
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
 - PxeDhcpv6GetOptionValue
---

# PxeDhcpv6GetOptionValue function


## -description

Retrieves an option value from a DHCPv6 packet.

## -parameters

### -param pPacket [in]

Pointer to a reply packet allocated with 
      the <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a> function.

### -param uPacketLen [in]

Length of the packet pointed to by the <i>pReplyPacket</i> parameter.

### -param uInstance [in]

One-based index that specifies which instance of the <i>wOption</i> parameter to 
      retrieve.

### -param wOption [in]

Option whose value will be retrieved.

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
The packet is not a valid DHCPv6 packet. This test is not as thorough as the tests used by the 
        <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxedhcpv6isvalid">PxeDhcpv6IsValid</a> function; only the packet length and 
        magic cookie are verified.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxedhcpv6appendoption">PxeDhcpv6AppendOption</a>



<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxedhcpv6getvendoroptionvalue">PxeDhcpv6GetVendorOptionValue</a>



<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxedhcpv6isvalid">PxeDhcpv6IsValid</a>



<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a>



<a href="/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>