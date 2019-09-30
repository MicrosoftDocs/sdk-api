---
UID: NN:vds.IVdsVolumeShrink
title: IVdsVolumeShrink (vds.h)
author: windows-sdk-content
description: Provides methods to support volume shrinking.
old-location: base\ivdsvolumeshrink.htm
tech.root: VDS
ms.assetid: 08c354a6-5cc0-405c-91cf-dca55b87b49a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsVolumeShrink, IVdsVolumeShrink interface, IVdsVolumeShrink interface,described, base.ivdsvolumeshrink, vds/IVdsVolumeShrink
ms.topic: interface
f1_keywords: 
 - "vds/IVdsVolumeShrink"
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IVdsVolumeShrink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsVolumeShrink interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to support volume shrinking.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVolumeShrink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsVolumeShrink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsVolumeShrink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumeshrink-querymaxreclaimablebytes">QueryMaxReclaimableBytes</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of bytes that can be reclaimed from the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumeshrink-shrink">Shrink</a>
</td>
<td align="left" width="63%">
Shrinks the volume and all plexes and returns the released extents.

</td>
</tr>
</table> 

