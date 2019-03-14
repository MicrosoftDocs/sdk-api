---
UID: NN:vds.IVdsSubSystem2
title: IVdsSubSystem2
author: windows-sdk-content
description: Provides methods for performing query and configuration operations on a subsystem using the VDS_HINTS2 and VDS_SUB_SYSTEM_PROP2 structures.
old-location: base\ivdssubsystem2.htm
tech.root: VDS
ms.assetid: 7d19792c-cd37-4ea7-8830-c33c489e63e6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsSubSystem2, IVdsSubSystem2 interface, IVdsSubSystem2 interface,described, base.ivdssubsystem2, vds/IVdsSubSystem2, vdshwprv/IVdsSubSystem2
ms.topic: interface
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
 - IVdsSubSystem2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsSubSystem2 interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods for performing query and configuration operations on a subsystem using the <a href="https://msdn.microsoft.com/e24935ac-17c8-4338-99cb-2408ca61da8a">VDS_HINTS2</a> and <a href="https://msdn.microsoft.com/8eb743b5-26e6-42e5-b94b-0849b1280cdb">VDS_SUB_SYSTEM_PROP2</a> structures.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsSubSystem2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsSubSystem2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsSubSystem2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fa046dd-fac9-4246-a90b-1837206b164c">CreateLun2</a>
</td>
<td align="left" width="63%">
Creates a LUN. This method is identical to the <a href="https://msdn.microsoft.com/e8097364-1f23-4cda-8f12-a750bbb4eb4c">IVdsSubSystem::CreateLun</a> method, except that automagic hints are provided using a <a href="https://msdn.microsoft.com/e24935ac-17c8-4338-99cb-2408ca61da8a">VDS_HINTS2</a> structure instead of a <a href="https://msdn.microsoft.com/2c9f04bb-a014-401e-9656-affbac11f810">VDS_HINTS</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5646da50-5ebd-44d8-b2e1-b3e96b9a6d3c">GetDrive2</a>
</td>
<td align="left" width="63%">
Returns the specified drive. This method is identical to the <a href="https://msdn.microsoft.com/855e9991-606c-4fcc-ba1d-ebdb928d4c3e">IVdsSubSystem::GetDrive</a> method, except that it includes the enclosure number as a parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f2164a9-643d-4762-8a2e-31d5c277502e">GetProperties2</a>
</td>
<td align="left" width="63%">
Returns the properties of a subsystem. This method is identical to the <a href="https://msdn.microsoft.com/cbcf1e14-7e3d-44e6-8c4a-afe927ed0f9d">IVdsSubSystem::GetProperties</a> method, except that it returns a <a href="https://msdn.microsoft.com/8eb743b5-26e6-42e5-b94b-0849b1280cdb">VDS_SUB_SYSTEM_PROP2</a> structure instead of a <a href="https://msdn.microsoft.com/8fecb874-5c59-4f55-b528-040ff9209612">VDS_SUB_SYSTEM_PROP</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6cd892d2-f1b0-40cd-b037-5c670da3b32f">QueryMaxLunCreateSize2</a>
</td>
<td align="left" width="63%">
Returns the size of the maximum LUN that can be created using the specified LUN type and hints. This method is identical to the <a href="https://msdn.microsoft.com/16e8bcab-d01f-494a-9705-8392cf043674">IVdsSubSystem::QueryMaxLunCreateSize</a> method, except that the automagic hints are provided using a <a href="https://msdn.microsoft.com/e24935ac-17c8-4338-99cb-2408ca61da8a">VDS_HINTS2</a> structure instead of a <a href="https://msdn.microsoft.com/2c9f04bb-a014-401e-9656-affbac11f810">VDS_HINTS</a> structure.

</td>
</tr>
</table> 

