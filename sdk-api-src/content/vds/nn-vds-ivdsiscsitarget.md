---
UID: NN:vds.IVdsIscsiTarget
title: IVdsIscsiTarget (vds.h)
author: windows-sdk-content
description: Provides methods for performing query and configuration operations on an iSCSI target.
old-location: base\ivdsiscsitarget.htm
tech.root: VDS
ms.assetid: 0db442c4-6cc1-43b2-8ac8-8b17cadb1101
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsIscsiTarget, IVdsIscsiTarget interface [VDS], IVdsIscsiTarget interface [VDS],described, base.ivdsiscsitarget, vds/IVdsIscsiTarget, vdshwprv/IVdsIscsiTarget
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
 - IVdsIscsiTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
---

# IVdsIscsiTarget interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides 
   methods for performing query and configuration operations on an iSCSI target.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsIscsiTarget</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsIscsiTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsIscsiTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c479b5ee-2e6a-4a3f-bd80-c3c25adac20f">CreatePortalGroup</a>
</td>
<td align="left" width="63%">
Creates a portal group.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a66077bf-7a08-49f6-9a32-da99aa1d218c">Delete</a>
</td>
<td align="left" width="63%">
Deletes the target and all of its portal groups if no LUNs are associated with the target.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2060f012-169c-4077-a6ed-cef362f926d4">GetConnectedInitiators</a>
</td>
<td align="left" width="63%">
Returns the list of iSCSI names of the initiators currently logged into the 
   target.

</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db48ec8e-aae1-4b88-9942-6a23de2cfe25">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of an iSCSI target.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9feb332-1b30-4de8-ac30-79fe53750d8c">GetSubSystem</a>
</td>
<td align="left" width="63%">
Returns the subsystem to which the target belongs.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f375c0b-7400-4660-8cb1-5291fd0dd52c">QueryAssociatedLuns</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the LUNs associated with the target.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bcddd435-a422-4ba3-8978-24388346ab27">QueryPortalGroups</a>
</td>
<td align="left" width="63%">
Returns an  enumeration of the iSCSI portal groups within the target.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3546f42c-2c30-4819-982d-9c186d9f858e">RememberInitiatorSharedSecret</a>
</td>
<td align="left" width="63%">
Communicates the initiator CHAP secret used for mutual CHAP authentication when the initiator 
     authenticates the target.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34afd8d7-473b-49c5-8486-2749144aea5c">SetFriendlyName</a>
</td>
<td align="left" width="63%">
Sets the friendly name of the target.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b2eae3d-8ad0-4b68-943b-a42696165543">SetSharedSecret</a>
</td>
<td align="left" width="63%">
Sets the target CHAP secret used for CHAP authentication when the target authenticates the 
     initiator.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

