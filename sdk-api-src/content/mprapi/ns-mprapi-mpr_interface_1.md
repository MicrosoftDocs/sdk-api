---
UID: NS:mprapi._MPR_INTERFACE_1
title: MPR_INTERFACE_1 (mprapi.h)
description: The MPR_INTERFACE_1 structure contains configuration and status information for a particular router interface.
helpviewer_keywords: ["*PMPR_INTERFACE_1","MPR_INTERFACE_1","MPR_INTERFACE_1 structure [RAS]","PMPR_INTERFACE_1","PMPR_INTERFACE_1 structure pointer [RAS]","_mpr_mpr_interface_1","mprapi/MPR_INTERFACE_1","mprapi/PMPR_INTERFACE_1","rras.mpr_interface_1"]
old-location: rras\mpr_interface_1.htm
tech.root: RRAS
ms.assetid: 90a3da46-7dd1-428b-ab72-d5defa710225
ms.date: 12/05/2018
ms.keywords: '*PMPR_INTERFACE_1, MPR_INTERFACE_1, MPR_INTERFACE_1 structure [RAS], PMPR_INTERFACE_1, PMPR_INTERFACE_1 structure pointer [RAS], _mpr_mpr_interface_1, mprapi/MPR_INTERFACE_1, mprapi/PMPR_INTERFACE_1, rras.mpr_interface_1'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: MPR_INTERFACE_1, *PMPR_INTERFACE_1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPR_INTERFACE_1
 - mprapi/_MPR_INTERFACE_1
 - PMPR_INTERFACE_1
 - mprapi/PMPR_INTERFACE_1
 - MPR_INTERFACE_1
 - mprapi/MPR_INTERFACE_1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - MPR_INTERFACE_1
---

# MPR_INTERFACE_1 structure


## -description

The 
<b>MPR_INTERFACE_1</b> structure contains configuration and status information for a particular router interface.

## -struct-fields

### -field wszInterfaceName

Pointer to a Unicode string that contains the name of the interface.

### -field hInterface

Handle to the interface.

### -field fEnabled

Specifies whether the interface is enabled. This value is <b>TRUE</b> if the interface is enabled, <b>FALSE</b> if the interface is administratively disabled.

### -field dwIfType

Specifies the 
<a href="/windows/desktop/api/mprapi/ne-mprapi-router_interface_type">type of interface</a>.

### -field dwConnectionState

Specifies the current state of the interface, for example connected, disconnected, or unreachable. For a list of possible states, see 
<a href="/windows/desktop/api/mprapi/ne-mprapi-router_connection_state">ROUTER_CONNECTION_STATE</a>.

### -field fUnReachabilityReasons

Specifies a value that represents a reason why the interface was unreachable. See 
<a href="/windows/desktop/RRAS/unreachability-reasons">Unreachability Reasons</a> for a list of possible values.

### -field dwLastError

Specifies a nonzero value if the interface fails to connect.

### -field lpwsDialoutHoursRestriction

Pointer to a Unicode string that specifies the times during which dial-out is restricted. The format for this string is: 





``` syntax
<day><space><time range><space><time range> . . . <NULL><day>. . . <NULL><NULL>

```

Where day is a numeral that corresponds to a day of the week.

<table>
<tr>
<th>Numeral</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Sunday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Monday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Tuesday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Wednesday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Thursday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Friday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Saturday

</td>
</tr>
</table>
 

Time range is of the form HH:MM-HH:MM, using 24-hour notation.

The string &lt;space&gt; in the preceding syntax denotes a space character. The string &lt;NULL&gt; denotes a null character.

The restriction string is terminated by two consecutive null characters.

Example:


``` syntax
2 09:00-12:00 13:00-17:30<NULL>4 09:00-12:00 13:00-17:30<NULL><NULL>

```

The preceding string restricts dial-out to Tuesdays and Thursdays from 9:00 AM to 12:00 PM and from 1:00 PM to 5:30 PM.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfaceenum">MprAdminInterfaceEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacegetinfo">MprAdminInterfaceGetInfo</a>



<a href="/windows/desktop/api/mprapi/ne-mprapi-router_connection_state">ROUTER_CONNECTION_STATE</a>



<a href="/windows/desktop/api/mprapi/ne-mprapi-router_interface_type">ROUTER_INTERFACE_TYPE</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>



<a href="/windows/desktop/RRAS/unreachability-reasons">Unreachability Reasons</a>
