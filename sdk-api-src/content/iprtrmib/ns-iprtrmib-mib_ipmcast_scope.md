---
UID: NS:iprtrmib._MIB_IPMCAST_SCOPE
title: MIB_IPMCAST_SCOPE (iprtrmib.h)
description: Contains a multicast scope name and the associated IPv4 multicast group address and mask that define the scope.
helpviewer_keywords: ["*PMIB_IPMCAST_SCOPE","MIB_IPMCAST_SCOPE","MIB_IPMCAST_SCOPE structure [MIB]","PMIB_IPMCAST_SCOPE","PMIB_IPMCAST_SCOPE structure pointer [MIB]","iprtrmib/MIB_IPMCAST_SCOPE","iprtrmib/PMIB_IPMCAST_SCOPE","mib.mib_ipmcast_scope"]
old-location: mib\mib_ipmcast_scope.htm
tech.root: MIB
ms.assetid: dbdbfdc6-becb-4ad5-9388-c2715d225fb0
ms.date: 12/05/2018
ms.keywords: '*PMIB_IPMCAST_SCOPE, MIB_IPMCAST_SCOPE, MIB_IPMCAST_SCOPE structure [MIB], PMIB_IPMCAST_SCOPE, PMIB_IPMCAST_SCOPE structure pointer [MIB], iprtrmib/MIB_IPMCAST_SCOPE, iprtrmib/PMIB_IPMCAST_SCOPE, mib.mib_ipmcast_scope'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MIB_IPMCAST_SCOPE, *PMIB_IPMCAST_SCOPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPMCAST_SCOPE
 - iprtrmib/_MIB_IPMCAST_SCOPE
 - PMIB_IPMCAST_SCOPE
 - iprtrmib/PMIB_IPMCAST_SCOPE
 - MIB_IPMCAST_SCOPE
 - iprtrmib/MIB_IPMCAST_SCOPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iprtrmib.h
api_name:
 - MIB_IPMCAST_SCOPE
---

# MIB_IPMCAST_SCOPE structure


## -description

The <b>MIB_IPMCAST_SCOPE</b> structure contains a multicast scope name and the associated IPv4 multicast group address and mask that define the scope.

## -struct-fields

### -field dwGroupAddress

Type: <b>DWORD</b>

A 32-bit integer representation of the IPv4 group address which, when combined with the corresponding value in <b>dwGroupMask</b>, identifies the group range for which the multicast scope exists. 

<div class="alert"><b>Note</b>  Scoped addresses must come from the range 239.*.*.* as specified in <a href="https://www.ietf.org/rfc/rfc2365.txt">RFC 2365</a>.</div>
<div> </div>

### -field dwGroupMask

Type: <b>DWORD</b>

A 32-bit integer representation of the IPv4 group address mask which, when combined with the corresponding value in <b>dwGroupAddress</b>, identifies the group range for which the multicast scope exists.

### -field snNameBuffer

Type: <b>WCHAR[256]</b>

A Unicode character array that contains the text name associated with the multicast scope. The name should be suitable for display to multicast application users.

If no name is specified, the default name is the string representation of the scoped address in <b>dwGroupAddress</b> with the address and mask length appended and separated by a slash "/" character, of the form "239.*.*.*.x/y", where <b>x</b> is the address length and <b>y</b> is the mask length.

### -field dwStatus

Type: <b>DWORD</b>

A status value that describes the current status of this row in a MFE scope table.

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
Row has <b>active</b> status.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Row has <b>notInService</b> status.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Row has <b>notReady</b> status.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Row has <b>createAndGo</b> status.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Row has <b>createAndWait</b> status.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Row has <b>destroy</b> status.

</td>
</tr>
</table>

## -remarks

Note that the <i>Iprtrmib.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Iprtrmib.h</i> header files should never be used directly.

