---
UID: NN:vdshwprv.IVdsLunMpio
title: IVdsLunMpio (vdshwprv.h)
description: Provides methods for performing query and configuration operations on a LUN with MPIO extensions.helpviewer_keywords: ["IVdsLunMpio","IVdsLunMpio interface [VDS]","IVdsLunMpio interface [VDS]","described","base.ivdslunmpio","vds/IVdsLunMpio","vdshwprv/IVdsLunMpio"]
old-location: base\ivdslunmpio.htm
tech.root: VDS
ms.assetid: 0c7ab50a-306e-44f8-976d-0e65e36b0fea
ms.date: 12/05/2018
ms.keywords: IVdsLunMpio, IVdsLunMpio interface [VDS], IVdsLunMpio interface [VDS],described, base.ivdslunmpio, vds/IVdsLunMpio, vdshwprv/IVdsLunMpio
f1_keywords:
- vdshwprv/IVdsLunMpio
dev_langs:
- c++
req.header: vdshwprv.h
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
- IVdsLunMpio
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsLunMpio interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods for performing 
   query and configuration operations on a LUN with MPIO extensions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsLunMpio</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsLunMpio</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsLunMpio</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunmpio-getloadbalancepolicy">GetLoadBalancePolicy</a>
</td>
<td align="left" width="63%">
Returns the current load balance policy on the LUN.</p> (Inherited from <b>IVdsLunMpio</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunmpio-getpathinfo">GetPathInfo</a>
</td>
<td align="left" width="63%">
Returns an array of <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_path_info">VDS_PATH_INFO</a> structures, 
     one for each path to the LUN.</p> (Inherited from <b>IVdsLunMpio</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunmpio-getsupportedlbpolicies">GetSupportedLbPolicies</a>
</td>
<td align="left" width="63%">
Retrieves the load balance policies that are supported by the hardware provider.</p> (Inherited from <b>IVdsLunMpio</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunmpio-setloadbalancepolicy">SetLoadBalancePolicy</a>
</td>
<td align="left" width="63%">
Sets the load balance policy on the LUN.</p> (Inherited from <b>IVdsLunMpio</b>)</td>
</tr>
</table> 


## -remarks



If your provider is an iSCSI provider, or if your provider does not support MPIO, you should not implement the <b>IVdsLunMpio</b> interface. If an iSCSI provider implements this interface, VDS will ignore it, because VDS uses the service's own routines to handle MPIO for iSCSI.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

