---
UID: NN:vsmgmt.IVssDifferentialSoftwareSnapshotMgmt3
title: IVssDifferentialSoftwareSnapshotMgmt3
author: windows-sdk-content
description: Defines methods that allow applications to use the shadow copy protection feature of VSS.
old-location: base\ivssdifferentialsoftwaresnapshotmgmt3.htm
old-project: VSS
ms.assetid: e5abcf69-748a-4ed6-973d-8ba49ec22ef2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IVssDifferentialSoftwareSnapshotMgmt3, IVssDifferentialSoftwareSnapshotMgmt3 interface, IVssDifferentialSoftwareSnapshotMgmt3 interface,described, base.ivssdifferentialsoftwaresnapshotmgmt3, vsmgmt/IVssDifferentialSoftwareSnapshotMgmt3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vsmgmt.h
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
tech.root: 
req.typenames: VSS_PROTECTION_LEVEL, *PVSS_PROTECTION_LEVEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsMgmt.h
api_name:
 - IVssDifferentialSoftwareSnapshotMgmt3
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssDifferentialSoftwareSnapshotMgmt3 interface


## -description


Defines methods that allow applications to use the shadow copy protection feature of VSS.

To obtain an instance of the <b>IVssDifferentialSoftwareSnapshotMgmt3</b> 
   interface, call the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> method of the 
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
 

 

