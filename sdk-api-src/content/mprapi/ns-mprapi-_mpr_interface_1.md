---
UID: NS:mprapi._MPR_INTERFACE_1
title: "_MPR_INTERFACE_1"
author: windows-sdk-content
description: The MPR_INTERFACE_1 structure contains configuration and status information for a particular router interface.
old-location: rras\mpr_interface_1.htm
tech.root: rras
ms.assetid: 90a3da46-7dd1-428b-ab72-d5defa710225
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: "*PMPR_INTERFACE_1, MPR_INTERFACE_1, MPR_INTERFACE_1 structure [RAS], PMPR_INTERFACE_1, PMPR_INTERFACE_1 structure pointer [RAS], _MPR_INTERFACE_1, _mpr_mpr_interface_1, mprapi/MPR_INTERFACE_1, mprapi/PMPR_INTERFACE_1, rras.mpr_interface_1"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - MPR_INTERFACE_1
product: Windows
targetos: Windows
req.typenames: MPR_INTERFACE_1, *PMPR_INTERFACE_1
req.redist: 
---

# _MPR_INTERFACE_1 structure


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
<a href="https://msdn.microsoft.com/9b957ab0-0c5d-4478-914a-4837e6bbd56a">type of interface</a>.


### -field dwConnectionState

Specifies the current state of the interface, for example connected, disconnected, or unreachable. For a list of possible states, see 
<a href="https://msdn.microsoft.com/e98f9843-c5a2-4714-8e22-58f24256d08f">ROUTER_CONNECTION_STATE</a>.


### -field fUnReachabilityReasons

Specifies a value that represents a reason why the interface was unreachable. See 
<a href="https://msdn.microsoft.com/55c0519e-02c8-4a04-bed9-9fe94327a4b6">Unreachability Reasons</a> for a list of possible values.


### -field dwLastError

Specifies a nonzero value if the interface fails to connect.


### -field lpwsDialoutHoursRestriction

Pointer to a Unicode string that specifies the times during which dial-out is restricted. The format for this string is: 




<pre class="syntax" xml:space="preserve"><code>&lt;day&gt;&lt;space&gt;&lt;time range&gt;&lt;space&gt;&lt;time range&gt; . . . &lt;NULL&gt;&lt;day&gt;. . . &lt;NULL&gt;&lt;NULL&gt;
</code></pre>
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

<pre class="syntax" xml:space="preserve"><code>2 09:00-12:00 13:00-17:30&lt;NULL&gt;4 09:00-12:00 13:00-17:30&lt;NULL&gt;&lt;NULL&gt;
</code></pre>
The preceding string restricts dial-out to Tuesdays and Thursdays from 9:00 AM to 12:00 PM and from 1:00 PM to 5:30 PM.


## -see-also




<a href="https://msdn.microsoft.com/c9590ebe-7e49-4ad1-bd9b-0d9c51938bc4">MprAdminInterfaceCreate</a>



<a href="https://msdn.microsoft.com/50486ad3-2f1d-4ab9-9a7f-7b72128486fb">MprAdminInterfaceEnum</a>



<a href="https://msdn.microsoft.com/a6d353f0-1d68-4a37-89f3-cdab0fc7972a">MprAdminInterfaceGetInfo</a>



<a href="https://msdn.microsoft.com/e98f9843-c5a2-4714-8e22-58f24256d08f">ROUTER_CONNECTION_STATE</a>



<a href="https://msdn.microsoft.com/9b957ab0-0c5d-4478-914a-4837e6bbd56a">ROUTER_INTERFACE_TYPE</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>



<a href="https://msdn.microsoft.com/55c0519e-02c8-4a04-bed9-9fe94327a4b6">Unreachability Reasons</a>
 

 

