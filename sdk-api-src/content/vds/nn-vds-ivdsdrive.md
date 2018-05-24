---
UID: NN:vds.IVdsDrive
title: IVdsDrive
author: windows-driver-content
description: Provides methods for performing query and configuration operations on a drive.
old-location: base\ivdsdrive.htm
old-project: VDS
ms.assetid: 597917cf-fb02-4949-98c3-3da3f7449ed1
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IVdsDrive, IVdsDrive interface [VDS], IVdsDrive interface [VDS],described, base.ivdsdrive, vds/IVdsDrive, vdshwprv/IVdsDrive
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsDrive
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsDrive interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods for performing query and configuration operations on a drive.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsDrive</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsDrive</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsDrive</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/195f0c13-40d7-4fad-b589-063ec4ff4efe">ClearFlags</a>
</td>
<td align="left" width="63%">
Clears all flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991811">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of the drive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e407cf77-93a7-48f6-85d3-007369316041">GetSubSystem</a>
</td>
<td align="left" width="63%">
Returns the subsystem to which the drive belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ee3e085-ce69-457e-b652-bb9c45b7fdd8">QueryExtents</a>
</td>
<td align="left" width="63%">
Returns an array of extents on a drive, including both allocated and unallocated extents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556703">SetFlags</a>
</td>
<td align="left" width="63%">
Sets flags on a drive object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d74f045f-7b6f-4ede-827d-f7f7486495e8">SetStatus</a>
</td>
<td align="left" width="63%">
Sets the status of the drive to the specified value.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2">Drive Object</a>



<a href="https://msdn.microsoft.com/e9ed5bdd-c696-47cc-84c8-266b230f7970">IVdsLunPlex::QueryExtents</a>



<a href="https://msdn.microsoft.com/855e9991-606c-4fcc-ba1d-ebdb928d4c3e">IVdsSubSystem::GetDrive</a>



<a href="https://msdn.microsoft.com/7d54922f-0531-4eab-afa9-f51ce6c75bfe">IVdsSubSystem::QueryDrives</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>



<a href="https://msdn.microsoft.com/c17f13f6-ccea-4370-84d1-b422efb63e73">VDS_DRIVE_PROP</a>
 

 

