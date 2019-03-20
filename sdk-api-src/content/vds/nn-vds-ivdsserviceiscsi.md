---
UID: NN:vds.IVdsServiceIscsi
title: IVdsServiceIscsi (vds.h)
author: windows-sdk-content
description: Provides methods to interface with the local initiator service, including the ability to set CHAP security settings and to log into targets.
old-location: base\ivdsserviceiscsi.htm
tech.root: VDS
ms.assetid: 07bbfb4b-f054-4ec2-8f0b-3910115db5c1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsServiceIscsi, IVdsServiceIscsi interface [VDS], IVdsServiceIscsi interface [VDS],described, base.ivdsserviceiscsi, vds/IVdsServiceIscsi
ms.topic: interface
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsServiceIscsi
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
---

# IVdsServiceIscsi interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods 
   to interface with the local initiator service, including the ability to set CHAP security settings and to log into 
   targets.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsServiceIscsi</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsServiceIscsi</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsServiceIscsi</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34f18293-6254-4f73-a633-642a3cdeaf31">GetInitiatorName</a>
</td>
<td align="left" width="63%">
Returns the iSCSI name of the local initiator service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/427d33e1-d2a5-46f3-a3be-d3589685f6af">QueryInitiatorAdapters</a>
</td>
<td align="left" width="63%">
Returns an object that enumerates the iSCSI initiator adapters of the initiator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fefe37aa-48c8-4ff4-b302-c6e95c1ffa5e">RememberTargetSharedSecret</a>
</td>
<td align="left" width="63%">
Communicates the CHAP secret of a target to the initiator service. This shared secret is used 
     during target login when the target authenticates the initiator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d76be416-c5e2-4b53-a1ff-0a27418c151e">SetAllIpsecSecurity</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05cf0347-a9f2-4f6f-b646-d7f71a6a6e70">SetAllIpsecTunnelAddresses</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90f9cf10-a0be-4ed1-8b0c-e6cc46384ba0">SetInitiatorSharedSecret</a>
</td>
<td align="left" width="63%">
Sets the initiator CHAP secret used for mutual CHAP authentication when the initiator 
     authenticates the target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d386eb3-5897-4ce7-91ab-99cf2bfa93bb">SetIpsecGroupPresharedKey</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

