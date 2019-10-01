---
UID: NN:vds.IVdsVolumeMF
title: IVdsVolumeMF (vds.h)
author: windows-sdk-content
description: Provides methods to perform access-path and file-system activities on the volume object.
old-location: base\ivdsvolumemf.htm
tech.root: VDS
ms.assetid: 4c8a63bd-ae2f-4157-92f9-aefc592c7d4f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsVolumeMF, IVdsVolumeMF interface [VDS], IVdsVolumeMF interface [VDS],described, base.ivdsvolumemf, vds/IVdsVolumeMF
ms.topic: interface
f1_keywords: 
 - "vds/IVdsVolumeMF"
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IVdsVolumeMF
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsVolumeMF interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to perform access-path and file-system activities on the volume object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVolumeMF</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsVolumeMF</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsVolumeMF</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf-addaccesspath">AddAccessPath</a>
</td>
<td align="left" width="63%">
Adds an access path. An access path can be a path to an empty folder or a drive letter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf-clearfilesystemflags">ClearFileSystemFlags</a>
</td>
<td align="left" width="63%">
Clears the file-system flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf-deleteaccesspath">DeleteAccessPath</a>
</td>
<td align="left" width="63%">
Deletes an access path from the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf-dismount">Dismount</a>
</td>
<td align="left" width="63%">
Dismounts a mounted volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf-format">Format</a>
</td>
<td align="left" width="63%">
Formats the file system on the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf-getfilesystemproperties">GetFileSystemProperties</a>
</td>
<td align="left" width="63%">
Returns property details about the file system on the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf-mount">Mount</a>
</td>
<td align="left" width="63%">
Mounts a volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf-queryaccesspaths">QueryAccessPaths</a>
</td>
<td align="left" width="63%">
Returns a list of all access paths, including the drive letter, to the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf-queryreparsepoints">QueryReparsePoints</a>
</td>
<td align="left" width="63%">
Returns all reparse points for the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf-setfilesystemflags">SetFileSystemFlags</a>
</td>
<td align="left" width="63%">
Sets the file-system flags.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/volume-object">Volume Object</a>
 

 

