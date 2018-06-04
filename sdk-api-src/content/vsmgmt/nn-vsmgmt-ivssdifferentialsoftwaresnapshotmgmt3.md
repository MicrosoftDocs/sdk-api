---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IVssDifferentialSoftwareSnapshotMgmt3 interface


## -description


Defines methods that allow applications to use the shadow copy protection feature of VSS.

To obtain an instance of the <b>IVssDifferentialSoftwareSnapshotMgmt3</b> 
   interface, call the <a href="_com_iunknown_queryinterface">QueryInterface</a> method of the 
   <a href="https://msdn.microsoft.com/d322981f-1916-4d38-9d05-bc3db2cd596d">IVssDifferentialSoftwareSnapshotMgmt</a> interface and pass 
   the <b>IID_IVssDifferentialSoftwareSnapshotMgmt3</b> constant as the interface identifier (IID) parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssDifferentialSoftwareSnapshotMgmt3</b> interface inherits from <a href="https://msdn.microsoft.com/b11d53cb-5b08-4798-acca-45237fc3e170">IVssDifferentialSoftwareSnapshotMgmt2</a> and <a href="https://msdn.microsoft.com/d322981f-1916-4d38-9d05-bc3db2cd596d">IVssDifferentialSoftwareSnapshotMgmt</a>. <b>IVssDifferentialSoftwareSnapshotMgmt3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssDifferentialSoftwareSnapshotMgmt3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07257d34-23b1-47bf-b613-f65f5d2a977e">ClearVolumeProtectFault</a>
</td>
<td align="left" width="63%">
Clears the protection fault state for the specified volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/daa23f2c-8342-4387-800a-def5951896ee">DeleteUnusedDiffAreas</a>
</td>
<td align="left" width="63%">
Deletes all shadow copy storage areas (also called diff areas) on the specified  volume that are not in use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a67bf9f1-135b-4881-acd1-6392f27d58e5">GetVolumeProtectLevel</a>
</td>
<td align="left" width="63%">
Gets the shadow copy protection level for the specified volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfa4420f-dc11-48c1-b177-1c58a4515550">QuerySnapshotDeltaBitmap</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f8f3a0c-5076-4ce3-aa8b-5c66ac5fa47a">SetVolumeProtectLevel</a>
</td>
<td align="left" width="63%">
Sets the shadow copy protection level for a volume.

</td>
</tr>
</table> 


## -remarks



An application with administrator privilege can use the <a href="https://msdn.microsoft.com/3f8f3a0c-5076-4ce3-aa8b-5c66ac5fa47a">SetVolumeProtectLevel</a> method to specify a shadow copy protection level for a volume and the separate volume that contains its shadow copy storage area. The same protection level should be set for both volumes. The possible protection levels are defined by the <a href="https://msdn.microsoft.com/f4c036ac-13fb-47be-8ad8-32c65caf0a2a">VSS_PROTECTION_LEVEL</a> enumeration.

When a volume protection fault occurs, the application must call the <a href="https://msdn.microsoft.com/a67bf9f1-135b-4881-acd1-6392f27d58e5">GetVolumeProtectLevel</a> method for the volume to identify the cause of the fault.




## -see-also




<a href="https://msdn.microsoft.com/d322981f-1916-4d38-9d05-bc3db2cd596d">IVssDifferentialSoftwareSnapshotMgmt</a>



<a href="https://msdn.microsoft.com/b11d53cb-5b08-4798-acca-45237fc3e170">IVssDifferentialSoftwareSnapshotMgmt2</a>
 

 

