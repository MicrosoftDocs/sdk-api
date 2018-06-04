---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _MIB_IPMCAST_SCOPE structure


## -description


The <b>MIB_IPMCAST_SCOPE</b> structure contains a multicast scope name and the associated IPv4 multicast group address and mask that define the scope.


## -struct-fields




### -field dwGroupAddress

Type: <b>DWORD</b>

A 32-bit integer representation of the IPv4 group address which, when combined with the corresponding value in <b>dwGroupMask</b>, identifies the group range for which the multicast scope exists. 

<div class="alert"><b>Note</b>  Scoped addresses must come from the range 239.*.*.* as specified in <a href="Http://go.microsoft.com/fwlink/p/?linkid=84040">RFC 2365</a>.</div>
<div> </div>

### -field dwGroupMask

Type: <b>DWORD</b>

A 32-bit integer representation of the IPv4 group address mask which, when combined with the corresponding value in <b>dwGroupAddress</b>, identifies the group range for which the multicast scope exists. 


### -field snNameBuffer

Type: <b>WCHAR[256]</b>

A Unicode character array that contains the text name associated with the multicast scope. The name should be suitable for display to multicast application users.

If no name is specified, the default name is the string representation of the scoped address in <b>dwGroupAddress</b> with the address and mask length appended and separated by a backslash "/" character, of the form "239.*.*.*.x/y", where <b>x</b> is the address length and<b> y</b> is the mask length.


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



