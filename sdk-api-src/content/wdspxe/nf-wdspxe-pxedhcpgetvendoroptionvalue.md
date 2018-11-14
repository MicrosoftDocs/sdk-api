---
UID: NF:wdspxe.PxeDhcpGetVendorOptionValue
title: PxeDhcpGetVendorOptionValue function
author: windows-sdk-content
description: Retrieves an option value from the Vendor Specific Information field (43) of a DHCP packet.
old-location: wds\pxedhcpgetvendoroptionvalue.htm
tech.root: wds
ms.assetid: 0cf14db2-b2e6-4e5e-a715-429bc0af7714
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: PxeDhcpGetVendorOptionValue, PxeDhcpGetVendorOptionValue function [Windows Deployment Services], wds.pxedhcpgetvendoroptionvalue, wdspxe/PxeDhcpGetVendorOptionValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsPxe.dll
api_name:
 - PxeDhcpGetVendorOptionValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- PxeDhcpGetVendorOptionValue
: 
---

# PxeDhcpGetVendorOptionValue function


## -description


Retrieves an option value from the Vendor Specific Information field (43) of a DHCP 
    packet.


## -parameters




### -param pPacket [in]

Pointer to a reply packet allocated with the 
      <a href="https://msdn.microsoft.com/f3a664a8-565c-4894-bea7-6664df0ecd9b">PxePacketAllocate</a> function.


### -param uPacketLen [in]

Length of the packet pointed to by the <i>pReplyPacket</i> parameter.


### -param bOption [in]

Option whose value will be retrieved.


### -param uInstance [in]

One-based index that specifies which instance of the <i>bOption</i> parameter to 
      retrieve.


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
        <a href="https://msdn.microsoft.com/b5f43afb-ab71-4edf-a48a-7315d19af913">PxeDhcpIsValid</a> function; only the packet length and 
        magic cookie are verified.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/831a830c-337c-4151-932b-db4783fc924e">PxeDhcpGetOptionValue</a>



<a href="https://msdn.microsoft.com/f3a664a8-565c-4894-bea7-6664df0ecd9b">PxePacketAllocate</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

