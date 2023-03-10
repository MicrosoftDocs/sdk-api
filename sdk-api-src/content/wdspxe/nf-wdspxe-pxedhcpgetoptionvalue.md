---
UID: NF:wdspxe.PxeDhcpGetOptionValue
title: PxeDhcpGetOptionValue function (wdspxe.h)
description: Retrieves an option value from a DHCP packet.
helpviewer_keywords: ["PxeDhcpGetOptionValue","PxeDhcpGetOptionValue function [Windows Deployment Services]","wds.pxedhcpgetoptionvalue","wdspxe/PxeDhcpGetOptionValue"]
old-location: wds\pxedhcpgetoptionvalue.htm
tech.root: wds
ms.assetid: 831a830c-337c-4151-932b-db4783fc924e
ms.date: 12/05/2018
ms.keywords: PxeDhcpGetOptionValue, PxeDhcpGetOptionValue function [Windows Deployment Services], wds.pxedhcpgetoptionvalue, wdspxe/PxeDhcpGetOptionValue
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
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
 - PxeDhcpGetOptionValue
 - wdspxe/PxeDhcpGetOptionValue
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
 - PxeDhcpGetOptionValue
---

# PxeDhcpGetOptionValue function


## -description

Retrieves an option value from a DHCP packet.

## -parameters

### -param pPacket [in]

Pointer to a reply packet allocated with 
      the <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a> function.

### -param uPacketLen [in]

Length of the packet pointed to by the <i>pReplyPacket</i> parameter.

### -param uInstance [in]

One-based index that specifies which instance of the <i>bOption</i> parameter to 
      retrieve.

### -param bOption [in]

Option whose value will be retrieved.

### -param pbOptionLen [out, optional]

Address of <b>BYTE</b> which will receive the length of the option value.

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
        <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxedhcpisvalid">PxeDhcpIsValid</a> function; only the packet length and 
        magic cookie are verified.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxedhcpappendoption">PxeDhcpAppendOption</a>



<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxedhcpgetvendoroptionvalue">PxeDhcpGetVendorOptionValue</a>



<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a>



<a href="/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>