---
UID: NN:vds.IVdsVolumeMF
title: IVdsVolumeMF
author: windows-sdk-content
description: Provides methods to perform access-path and file-system activities on the volume object.
old-location: base\ivdsvolumemf.htm
tech.root: VDS
ms.assetid: 4c8a63bd-ae2f-4157-92f9-aefc592c7d4f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsVolumeMF, IVdsVolumeMF interface [VDS], IVdsVolumeMF interface [VDS],described, base.ivdsvolumemf, vds/IVdsVolumeMF
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsVolumeMF interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to perform access-path and file-system activities on the volume object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVolumeMF</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsVolumeMF</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/cf29639e-33fd-42f6-b616-7145521da347">AddAccessPath</a>
</td>
<td align="left" width="63%">
Adds an access path. An access path can be a path to an empty folder or a drive letter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3b02b4a-109c-419f-94c1-fc2f15ea5291">ClearFileSystemFlags</a>
</td>
<td align="left" width="63%">
Clears the file-system flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05020390-475f-4528-ba44-ecdfe008149f">DeleteAccessPath</a>
</td>
<td align="left" width="63%">
Deletes an access path from the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ef5a1e6-0e41-4077-9ae8-fe266f2623cc">Dismount</a>
</td>
<td align="left" width="63%">
Dismounts a mounted volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8203ac16-99af-4962-bafc-12c0d238d062">Format</a>
</td>
<td align="left" width="63%">
Formats the file system on the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43f5495c-5a60-44fd-b217-16464c4693a4">GetFileSystemProperties</a>
</td>
<td align="left" width="63%">
Returns property details about the file system on the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1de3bbd7-cd81-42f9-9e25-48a0a07e9ccc">Mount</a>
</td>
<td align="left" width="63%">
Mounts a volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d541245-c189-4abe-ac72-2928c7aeed95">QueryAccessPaths</a>
</td>
<td align="left" width="63%">
Returns a list of all access paths, including the drive letter, to the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae79355d-2012-42bf-930d-2915c4ca502c">QueryReparsePoints</a>
</td>
<td align="left" width="63%">
Returns all reparse points for the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/836f4a8d-8736-4876-8de3-a6265d7eb66a">SetFileSystemFlags</a>
</td>
<td align="left" width="63%">
Sets the file-system flags.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>



<a href="https://msdn.microsoft.com/92013015-b0f5-4b92-937b-c2637f65810c">Volume Object</a>
 

 

