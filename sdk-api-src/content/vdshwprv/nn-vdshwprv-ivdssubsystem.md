---
UID: NN:vdshwprv.IVdsSubSystem
title: IVdsSubSystem
author: windows-sdk-content
description: Provides methods for performing query and configuration operations on a subsystem.
old-location: base\ivdssubsystem.htm
old-project: VDS
ms.assetid: 1f1b9735-216b-4bc5-a9b8-2d274827b2c8
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IVdsSubSystem, IVdsSubSystem interface [VDS], IVdsSubSystem interface [VDS],described, base.ivdssubsystem, vds/IVdsSubSystem, vdshwprv/IVdsSubSystem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vdshwprv.h
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
tech.root: 
req.typenames: VDS_VERSION_SUPPORT_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsSubSystem
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsSubSystem interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods for performing query and configuration operations on a subsystem.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsSubSystem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsSubSystem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsSubSystem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8097364-1f23-4cda-8f12-a750bbb4eb4c">CreateLun</a>
</td>
<td align="left" width="63%">
Creates a new LUN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/855e9991-606c-4fcc-ba1d-ebdb928d4c3e">GetDrive</a>
</td>
<td align="left" width="63%">
Returns the specified drive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991811">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of the subsystem object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/317e4aa3-2635-4e1b-af2d-ad7c6170bf33">GetProvider</a>
</td>
<td align="left" width="63%">
Returns the provider that manages the subsystem.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61f32915-c616-477e-b0f0-4a7f92aca0e2">QueryControllers</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the controllers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d54922f-0531-4eab-afa9-f51ce6c75bfe">QueryDrives</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the drives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8e17085-03cd-40d1-accf-6ea5fa69de65">QueryLuns</a>
</td>
<td align="left" width="63%">
Returns an enumeration of LUNs surfaced by the subsystem.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16e8bcab-d01f-494a-9705-8392cf043674">QueryMaxLunCreateSize</a>
</td>
<td align="left" width="63%">
Returns the size of the maximum  LUN that can be created using the specified 
    LUN type and hints.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d6118bb-7b13-4ae1-9faf-9c17ada20511">Reenumerate</a>
</td>
<td align="left" width="63%">
Prompts the subsystem to scan its bus to discover newly connected drives or newly disconnected drives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/349fa2aa-94cd-4db0-9682-c39bcd9f9109">ReplaceDrive</a>
</td>
<td align="left" width="63%">
Replaces or migrates one of the drives with another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/080a48a5-1c25-440a-ad3c-528cdaef40e9">SetControllerStatus</a>
</td>
<td align="left" width="63%">
Sets the controllers to either online or offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07104aac-acdc-447c-9a30-ff3318f6df09">SetStatus</a>
</td>
<td align="left" width="63%">
Sets the status of the subsystem to the specified value.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8635d594-b58a-4ee1-9966-1340d954da81">IVdsController::GetSubSystem</a>



<a href="https://msdn.microsoft.com/e407cf77-93a7-48f6-85d3-007369316041">IVdsDrive::GetSubSystem</a>



<a href="https://msdn.microsoft.com/ae327655-3db9-44b0-934a-458ee90b1d07">IVdsHwProvider::QuerySubSystems</a>



<a href="https://msdn.microsoft.com/bd7dbe48-ad56-4304-a076-608f697620d8">IVdsLun::GetSubSystem</a>



<a href="https://msdn.microsoft.com/f605a5de-9256-4b43-8e12-3d78fd6cd9f1">Subsystem Object</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

