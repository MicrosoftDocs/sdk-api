---
UID: NF:wdspxe.PxeDhcpv6GetOptionValue
title: PxeDhcpv6GetOptionValue function (wdspxe.h)
author: windows-sdk-content
description: Retrieves an option value from a DHCPv6 packet.
old-location: wds\pxedhcpv6getoptionvalue.htm
tech.root: wds
ms.assetid: 0DC0CF7F-0C74-4595-9DC6-9468E1E7DA20
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PxeDhcpv6GetOptionValue, PxeDhcpv6GetOptionValue function [Windows Deployment Services], wds.pxedhcpv6getoptionvalue, wdspxe/PxeDhcpv6GetOptionValue
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsPxe.dll
api_name:
 - PxeDhcpv6GetOptionValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PxeDhcpv6GetOptionValue function


## -description


Retrieves an option value from a DHCPv6 packet.


## -parameters




### -param pPacket [in]

Pointer to a reply packet allocated with 
      the <a href="https://msdn.microsoft.com/f3a664a8-565c-4894-bea7-6664df0ecd9b">PxePacketAllocate</a> function.


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
        <a href="https://msdn.microsoft.com/E20A9E7A-8CFA-4A2B-8A40-7937937332A5">PxeDhcpv6IsValid</a> function; only the packet length and 
        magic cookie are verified.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/92A35846-360B-42D3-935B-6FC10AF687A5">PxeDhcpv6AppendOption</a>



<a href="https://msdn.microsoft.com/9F969C0C-93CA-4355-8556-2F43542570F1">PxeDhcpv6GetVendorOptionValue</a>



<a href="https://msdn.microsoft.com/E20A9E7A-8CFA-4A2B-8A40-7937937332A5">PxeDhcpv6IsValid</a>



<a href="https://msdn.microsoft.com/f3a664a8-565c-4894-bea7-6664df0ecd9b">PxePacketAllocate</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

