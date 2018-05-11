---
UID: NF:mgm.MgmDeleteGroupMembershipEntry
title: MgmDeleteGroupMembershipEntry function
author: windows-driver-content
description: The MgmDeleteGroupMembershipEntry function notifies the multicast group manager that there are no more receivers present for the specified groups on the specified interface.
old-location: rras\mgmdeletegroupmembershipentry.htm
old-project: RRAS
ms.assetid: fe39d824-3154-4479-bd70-09b2b6593885
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MGM_FORWARD_STATE, MGM_JOIN_STATE_FLAG, MgmDeleteGroupMembershipEntry, MgmDeleteGroupMembershipEntry function [RAS], _mpr_mgmdeletegroupmembershipentry, mgm/MgmDeleteGroupMembershipEntry, rras.mgmdeletegroupmembershipentry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mgm.h
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
req.typenames: MGM_ENUM_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rtm.dll
api_name:
-	MgmDeleteGroupMembershipEntry
product: Windows
targetos: Windows
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
req.product: GDI+ 1.1
---

# MgmDeleteGroupMembershipEntry function


## -description


The 
<b>MgmDeleteGroupMembershipEntry</b> function notifies the multicast group manager that there are no more receivers present for the specified groups on the specified interface.

A multicast routing protocol calls this function after it is notified that there are no more receivers for a multicast group on an interface. The protocol must call this function to stop multicast data from being forwarded out over an interface.


## -parameters




### -param hProtocol [in]

Handle to the protocol obtained from a previous call to 
<a href="https://msdn.microsoft.com/a9b5f5f3-6e54-4a97-b3e7-e9e026947116">MgmRegisterMProtocol</a>.


### -param dwSourceAddr [in]

Specifies the source address from which to stop receiving multicast data. Specify zero to stop receiving data from all sources (a wildcard receiver for a group); otherwise, specify the IP address of the source or source network. 




To specify a range of source addresses, specify the source network using <i>dwSourceAddr</i>, and specify a subnet mask using <i>dwSourceMask</i>.


### -param dwSourceMask [in]

Specifies the subnet mask that corresponds to <i>dwSourceAddr</i>. The <i>dwSourceAddr</i> and <i>dwSourceMask</i> parameters are used together to define a range of sources from which to stop receiving multicast data. 




Specify zero for this parameter if zero was specified for <i>dwSourceAddr</i> (a wildcard receiver).
						


### -param dwGroupAddr [in]

Specifies the multicast group for which to stop receiving data. Specify zero to stop receiving all groups (a wildcard receiver); otherwise, specify the IP address of the group. 




To specify a range of group addresses, specify the group address using <i>dwGroupAddr</i>, and specify a subnet mask using <i>dwGroupMask</i>.


### -param dwGroupMask [in]

Specifies the subnet mask that corresponds to <i>dwGroupAddr</i>. The <i>dwGroupAddr</i> and <i>dwGroupMask</i> parameters are used together to define a range of multicast groups. 




Specify zero for this parameter if zero was specified for <i>dwGroupAddr</i> (a wildcard receiver).


### -param dwIfIndex [in]

Specifies the interface on which to delete the group membership. Multicast data for the specified groups are no longer  forwarded out over this interface.


### -param dwIfNextHopIPAddr [in]

Specifies the address of the next hop that corresponds to the index specified by <i>dwIfIndex</i>. The <i>dwIfIndex</i> and <i>dwIfNextHopIPAddr</i> parameters uniquely identify a next hop on point-to-multipoint interfaces. A point-to-multipoint interface is a connection where one interface connects to multiple networks. Examples of point-to-multipoint interfaces include non-broadcast multiple access (NBMA) interfaces and the internal interface on which all dial-up clients connect. 




For broadcast interfaces (such as Ethernet interfaces) or point-to-point interfaces, which are identified by only the value of <i>dwIfIndex</i>, specify zero.


### -param dwFlags [in]

Specifies any additional processing that must take place when the group membership is removed. Valid values are: 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MGM_JOIN_STATE_FLAG"></a><a id="mgm_join_state_flag"></a><dl>
<dt><b>MGM_JOIN_STATE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Remove group membership for the specified source and group. Update any forwarding entries for the specified source group to reflect this change in group membership.

</td>
</tr>
<tr>
<td width="40%"><a id="MGM_FORWARD_STATE"></a><a id="mgm_forward_state"></a><dl>
<dt><b>MGM_FORWARD_STATE</b></dt>
</dl>
</td>
<td width="60%">
Remove the specified interface from the list of outgoing interfaces for the forwarding entry that corresponds to the specified source and group.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Could not complete the call to this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Invalid handle to a protocol, or the interface is owned by another protocol.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified interface was not found.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



This version of the MGM API supports only wildcard sources or specific sources, not a range of sources. The same restriction applies to groups (that is, no group ranges are permitted).

When this function is called, the multicast group manager may invoke the 
<a href="https://msdn.microsoft.com/1c23df04-2a31-475e-a8da-783796a60e00">PMGM_PRUNE_ALERT_CALLBACK</a> callback to notify other routing protocols that no more receivers are present for the specified group.




## -see-also




<a href="https://msdn.microsoft.com/b767961e-0935-4662-9f54-d82dfa0e7bd0">MgmAddGroupMembershipEntry</a>



<a href="https://msdn.microsoft.com/1c23df04-2a31-475e-a8da-783796a60e00">PMGM_PRUNE_ALERT_CALLBACK</a>
 

 

