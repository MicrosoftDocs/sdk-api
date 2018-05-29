---
UID: NS:iprtrmib._MIB_IPMCAST_BOUNDARY
title: "_MIB_IPMCAST_BOUNDARY"
author: windows-sdk-content
description: Contains a row in a MIB_IPMCAST_BOUNDARY_TABLE structure that lists a router's scoped IPv4 multicast address boundaries.
old-location: mib\mib_ipmcast_boundary.htm
old-project: MIB
ms.assetid: a3d900be-14c9-4ad9-bc2e-382849a6d1c6
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: "*PMIB_IPMCAST_BOUNDARY, MIB_IPMCAST_BOUNDARY, MIB_IPMCAST_BOUNDARY structure [MIB], PMIB_IPMCAST_BOUNDARY, PMIB_IPMCAST_BOUNDARY structure pointer [MIB], _MIB_IPMCAST_BOUNDARY, iprtrmib/MIB_IPMCAST_BOUNDARY, iprtrmib/PMIB_IPMCAST_BOUNDARY, mib.mib_ipmcast_boundary"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iprtrmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MIB_IPMCAST_BOUNDARY, *PMIB_IPMCAST_BOUNDARY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iprtrmib.h
api_name:
-	MIB_IPMCAST_BOUNDARY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MIB_IPMCAST_BOUNDARY structure


## -description


The <b>MIB_IPMCAST_BOUNDARY</b> structure contains a row in a <a href="https://msdn.microsoft.com/afa93943-efc7-430f-b8d0-4e79132278e2">MIB_IPMCAST_BOUNDARY_TABLE</a> structure that lists a router's scoped IPv4 multicast address boundaries.


## -struct-fields




### -field dwIfIndex

Type: <b>DWORD</b>

The index value for the interface to which this boundary applies. Packets with a destination address in the associated address/mask range are not forwarded with this interface.


### -field dwGroupAddress

Type: <b>DWORD</b>

The 32-bit integer representation of the IPv4 group address which, when combined with the corresponding value in <b>dwGroupMask</b>, identifies the group range for which the scoped boundary exists. 

<div class="alert"><b>Note</b>  Scoped addresses must come from the range 239.*.*.* as specified in <a href="Http://go.microsoft.com/fwlink/p/?linkid=84040">RFC 2365</a>.</div>
<div> </div>

### -field dwGroupMask

Type: <b>DWORD</b>

The 32-bit integer representation of the IPv4 group address mask which, when combined with the corresponding value in <b>dwGroupAddress</b>, identifies the group range for which the scoped boundary exists. 


### -field dwStatus

Type: <b>DWORD</b>

A status value that describes the current status of this entry in a MFE boundary table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The entry has <b>active</b> status.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The entry has <b>notInService</b> status.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The entry  has <b>notReady</b> status.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The entry has <b>createAndGo</b> status.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The entry has <b>createAndWait</b> status.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The entry has <b>destroy</b> status.

</td>
</tr>
</table>
 


## -remarks



Note that the <i>Iprtrmib.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Iprtrmib.h</i> header file should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/afa93943-efc7-430f-b8d0-4e79132278e2">MIB_IPMCAST_BOUNDARY_TABLE</a>
 

 

