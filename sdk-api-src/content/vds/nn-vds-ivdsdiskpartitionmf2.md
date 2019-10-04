---
UID: NN:vds.IVdsDiskPartitionMF2
title: IVdsDiskPartitionMF2 (vds.h)
author: windows-sdk-content
description: Provides a method to format a partition with additional formatting options.
old-location: base\ivdsdiskpartitionmf2.htm
tech.root: VDS
ms.assetid: 94a8ef66-3daf-46d4-be5f-dd56739c773a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsDiskPartitionMF2, IVdsDiskPartitionMF2 interface, IVdsDiskPartitionMF2 interface,described, base.ivdsdiskpartitionmf2, vds/IVdsDiskPartitionMF2
ms.topic: interface
f1_keywords: 
 - "vds/IVdsDiskPartitionMF2"
dev_langs:
 - c++
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - COM
api_location:
 - Vds.h
api_name:
 - IVdsDiskPartitionMF2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsDiskPartitionMF2 interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides a method to format a partition with additional formatting options.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsDiskPartitionMF2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsDiskPartitionMF2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsDiskPartitionMF2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdiskpartitionmf2-formatpartitionex2">FormatPartitionEx2</a>
</td>
<td align="left" width="63%">
Formats an existing OEM, ESP, or unknown partition. This method is identical to the <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-formatpartition">IVdsDiskPartitionMF::FormatPartition</a> method, except that formatting options are specified by using the <i>Options</i> parameter.

</td>
</tr>
</table> 

