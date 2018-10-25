---
UID: NF:mgm.MgmReleaseInterfaceOwnership
title: MgmReleaseInterfaceOwnership function
author: windows-sdk-content
description: The MgmReleaseInterfaceOwnership function is used by a client to relinquish ownership of an interface. When this function is called, all MFEs maintained by the multicast group manager on behalf of the client and for the specified interface are deleted.
old-location: rras\mgmreleaseinterfaceownership.htm
tech.root: rras
ms.assetid: 501970f7-7728-4a83-8f4b-207579d65d01
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: MgmReleaseInterfaceOwnership, MgmReleaseInterfaceOwnership function [RAS], _mpr_mgmreleaseinterfaceownership, mgm/MgmReleaseInterfaceOwnership, rras.mgmreleaseinterfaceownership
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
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - MgmReleaseInterfaceOwnership
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MgmReleaseInterfaceOwnership function


## -description


The 
<b>MgmReleaseInterfaceOwnership</b> function is used by a client to relinquish ownership of an interface. When this function is called, all MFEs maintained by the multicast group manager on behalf of the client and for the specified interface are deleted.


## -parameters




### -param hProtocol [in]

Handle to the protocol obtained from a previous call to 
<a href="https://msdn.microsoft.com/a9b5f5f3-6e54-4a97-b3e7-e9e026947116">MgmRegisterMProtocol</a>.


### -param dwIfIndex [in]

Specifies the index of the interface to release.


### -param dwIfNextHopAddr [in]

Specifies the address of the next hop that corresponds to the index specified by <i>dwIfIndex</i>. The <i>dwIfIndex</i> and <i>dwIfNextHopIPAddr</i> parameters uniquely identify a next hop on point-to-multipoint interfaces. A point-to-multipoint interface is a connection where one interface connects to multiple networks. Examples of point-to-multipoint interfaces include non-broadcast multiple access (NBMA) interfaces and the internal interface on which all dial-up clients connect. 




For broadcast interfaces (such as Ethernet interfaces) or point-to-point interfaces, which are identified by only the value of <i>dwIfIndex</i>, specify zero.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes:

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
Invalid handle to a client, or the interface was not found.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



A client must release ownership of all the interfaces it owns before deregistering itself with the 
<a href="https://msdn.microsoft.com/e9b2613e-4e52-4993-81dd-0be50a072db6">MgmDeRegisterMProtocol</a> function.




## -see-also




<a href="https://msdn.microsoft.com/e9b2613e-4e52-4993-81dd-0be50a072db6">MgmDeRegisterMProtocol</a>



<a href="https://msdn.microsoft.com/b072c884-0b84-4dd9-a14c-185f5d327017">MgmTakeInterfaceOwnership</a>
 

 

