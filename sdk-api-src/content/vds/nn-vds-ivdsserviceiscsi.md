---
UID: NN:vds.IVdsServiceIscsi
title: IVdsServiceIscsi (vds.h)
author: windows-sdk-content
description: Provides methods to interface with the local initiator service, including the ability to set CHAP security settings and to log into targets.
old-location: base\ivdsserviceiscsi.htm
tech.root: VDS
ms.assetid: 07bbfb4b-f054-4ec2-8f0b-3910115db5c1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsServiceIscsi, IVdsServiceIscsi interface [VDS], IVdsServiceIscsi interface [VDS],described, base.ivdsserviceiscsi, vds/IVdsServiceIscsi
ms.topic: interface
f1_keywords: 
 - "vds/IVdsServiceIscsi"
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
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
---

# IVdsServiceIscsi interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods 
   to interface with the local initiator service, including the ability to set CHAP security settings and to log into 
   targets.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsServiceIscsi</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsServiceIscsi</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsserviceiscsi-getinitiatorname">GetInitiatorName</a>
</td>
<td align="left" width="63%">
Returns the iSCSI name of the local initiator service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsserviceiscsi-queryinitiatoradapters">QueryInitiatorAdapters</a>
</td>
<td align="left" width="63%">
Returns an object that enumerates the iSCSI initiator adapters of the initiator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsserviceiscsi-remembertargetsharedsecret">RememberTargetSharedSecret</a>
</td>
<td align="left" width="63%">
Communicates the CHAP secret of a target to the initiator service. This shared secret is used 
     during target login when the target authenticates the initiator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsserviceiscsi-setallipsecsecurity">SetAllIpsecSecurity</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsserviceiscsi-setallipsectunneladdresses">SetAllIpsecTunnelAddresses</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsserviceiscsi-setinitiatorsharedsecret">SetInitiatorSharedSecret</a>
</td>
<td align="left" width="63%">
Sets the initiator CHAP secret used for mutual CHAP authentication when the initiator 
     authenticates the target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsserviceiscsi-setipsecgrouppresharedkey">SetIpsecGroupPresharedKey</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

