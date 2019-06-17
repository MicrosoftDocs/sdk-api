---
UID: NN:vdshwprv.IVdsLunNaming
title: IVdsLunNaming (vdshwprv.h)
author: windows-sdk-content
description: Provides a method to name LUNs for a class implementing the IVdsLun interface.
old-location: base\ivdslunnaming.htm
tech.root: VDS
ms.assetid: 1cc5fbb2-6a40-4b7c-9b5f-8f5fb53e6173
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsLunNaming, IVdsLunNaming interface [VDS], IVdsLunNaming interface [VDS],described, base.ivdslunnaming, vds/IVdsLunNaming, vdshwprv/IVdsLunNaming
ms.topic: interface
f1_keywords: ["vdshwprv/IVdsLunNaming"]
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
 - IVdsLunNaming
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsLunNaming interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides a method to name 
   LUNs for a class implementing the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslun">IVdsLun</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsLunNaming</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsLunNaming</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsLunNaming</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunnaming-setfriendlyname">SetFriendlyName</a>
</td>
<td align="left" width="63%">
Sets the friendly name of a LUN.</p> (Inherited from <b>IVdsLunNaming</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

