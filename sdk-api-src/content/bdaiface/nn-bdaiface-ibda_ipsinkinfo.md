---
UID: NN:bdaiface.IBDA_IPSinkInfo
title: IBDA_IPSinkInfo
author: windows-driver-content
description: This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.
old-location: mstv\ibda_ipsinkinfo.htm
old-project: mstv
ms.assetid: fbbe12ea-964a-4a83-ac0a-ac8808bd9a63
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IBDA_IPSinkInfo, IBDA_IPSinkInfo interface [Microsoft TV Technologies], IBDA_IPSinkInfo interface [Microsoft TV Technologies], described, IBDA_IPSinkInfoInterface, bdaiface/IBDA_IPSinkInfo, mstv.ibda_ipsinkinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_IPSinkInfo
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IBDA_IPSinkInfo interface


## -description



This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
        

The <b>IBDA_IPSinkInfo</b> interface is implemented on the <a href="https://msdn.microsoft.com/78cd6cba-3bd7-4ad4-b65d-c6b866a18d4e">BDA IP Sink</a> filter, which manages the delivery of in-band IP data to the network stack. This interface supersedes <a href="https://msdn.microsoft.com/3665c06e-0e9f-4a8a-bb72-eb0c402ce7c9">IBDA_IPSinkControl</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_IPSinkInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_IPSinkInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_IPSinkInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68b41304-2043-4cbf-8872-7f3d9f3b7a83">get_AdapterDescription</a>
</td>
<td align="left" width="63%">
Retrieves the description of the network adapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3518bad7-d732-4ef7-a8b6-135193eaf9d6">get_AdapterIPAddress</a>
</td>
<td align="left" width="63%">
Retrieves the IP address of the data that the IP Sink filter receives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29375c69-5e45-4fc5-98d2-1cc1c750b809">get_MulticastList</a>
</td>
<td align="left" width="63%">
Retrieves a list of the multicast addresses to which the IP Sink filter is listening.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_IPSinkInfo)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

