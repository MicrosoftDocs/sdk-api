---
UID: NN:vds.IVdsServiceSAN
title: IVdsServiceSAN (vds.h)
author: windows-sdk-content
description: Provides methods for managing disk online and offline SAN policy for the operating system.
old-location: base\ivdsservicesan.htm
tech.root: VDS
ms.assetid: 675e9ea8-06b6-4832-9311-17361e4781d4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsServiceSAN, IVdsServiceSAN interface, IVdsServiceSAN interface,described, base.ivdsservicesan, vds/IVdsServiceSAN
ms.topic: interface
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IVdsServiceSAN
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsServiceSAN interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods for managing disk online and offline <a href="https://docs.microsoft.com/windows/desktop/api/vds/ne-vds-_vds_san_policy">SAN policy</a> for the operating system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsServiceSAN</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsServiceSAN</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsServiceSAN</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservicesan-getsanpolicy">GetSANPolicy</a>
</td>
<td align="left" width="63%">
Gets the disk SAN policy for the operating system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservicesan-setsanpolicy">SetSANPolicy</a>
</td>
<td align="left" width="63%">
Sets the disk SAN policy for the operating system.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/ne-vds-_vds_san_policy">VDS_SAN_POLICY</a>
 

 

