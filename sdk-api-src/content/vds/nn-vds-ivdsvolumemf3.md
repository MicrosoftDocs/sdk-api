---
UID: NN:vds.IVdsVolumeMF3
title: IVdsVolumeMF3 (vds.h)
author: windows-sdk-content
description: Provides methods to perform additional file system management operations on the volume object.
old-location: base\ivdsvolumemf3.htm
tech.root: VDS
ms.assetid: 46b8ff26-c00b-45ef-ac30-0aa82786bf9b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsVolumeMF3, IVdsVolumeMF3 interface, IVdsVolumeMF3 interface,described, base.ivdsvolumemf3, vds/IVdsVolumeMF3
ms.topic: interface
f1_keywords: 
 - "vds/IVdsVolumeMF3"
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
 - IVdsVolumeMF3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsVolumeMF3 interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

 Provides methods to perform additional file system management operations on the volume object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVolumeMF3</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsVolumeMF3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsVolumeMF3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf3-formatex2">FormatEx2</a>
</td>
<td align="left" width="63%">
Formats a file system volume on a partition. This method is identical to the <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf2-formatex">IVdsVolumeMF2::FormatEx</a> method, except that formatting options are specified by using the <i>Options</i> parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf3-offlinevolume">OfflineVolume</a>
</td>
<td align="left" width="63%">
Takes the volume offline by using the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_volume_offline">IOCTL_VOLUME_OFFLINE</a> control code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf3-queryvolumeguidpathnames">QueryVolumeGuidPathnames</a>
</td>
<td align="left" width="63%">
Returns a list of volume GUID paths for the current volume.

</td>
</tr>
</table> 

