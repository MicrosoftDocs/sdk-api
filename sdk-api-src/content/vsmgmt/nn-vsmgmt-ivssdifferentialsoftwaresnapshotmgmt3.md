---
UID: NN:vsmgmt.IVssDifferentialSoftwareSnapshotMgmt3
title: IVssDifferentialSoftwareSnapshotMgmt3 (vsmgmt.h)

description: Defines methods that allow applications to use the shadow copy protection feature of VSS.
old-location: base\ivssdifferentialsoftwaresnapshotmgmt3.htm
tech.root: VSS
ms.assetid: e5abcf69-748a-4ed6-973d-8ba49ec22ef2

ms.date: 12/05/2018
ms.keywords: IVssDifferentialSoftwareSnapshotMgmt3, IVssDifferentialSoftwareSnapshotMgmt3 interface, IVssDifferentialSoftwareSnapshotMgmt3 interface,described, base.ivssdifferentialsoftwaresnapshotmgmt3, vsmgmt/IVssDifferentialSoftwareSnapshotMgmt3
ms.topic: interface
f1_keywords:
- vsmgmt/IVssDifferentialSoftwareSnapshotMgmt3
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- VsMgmt.h
api_name:
- IVssDifferentialSoftwareSnapshotMgmt3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssDifferentialSoftwareSnapshotMgmt3 interface


## -description


Defines methods that allow applications to use the shadow copy protection feature of VSS.

To obtain an instance of the <b>IVssDifferentialSoftwareSnapshotMgmt3</b> 
   interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method of the 
   <a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt">IVssDifferentialSoftwareSnapshotMgmt</a> interface and pass 
   the <b>IID_IVssDifferentialSoftwareSnapshotMgmt3</b> constant as the interface identifier (IID) parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssDifferentialSoftwareSnapshotMgmt3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2">IVssDifferentialSoftwareSnapshotMgmt2</a> and <a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt">IVssDifferentialSoftwareSnapshotMgmt</a>. <b>IVssDifferentialSoftwareSnapshotMgmt3</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3-clearvolumeprotectfault">ClearVolumeProtectFault</a>
</td>
<td align="left" width="63%">
Clears the protection fault state for the specified volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3-deleteunuseddiffareas">DeleteUnusedDiffAreas</a>
</td>
<td align="left" width="63%">
Deletes all shadow copy storage areas (also called diff areas) on the specified  volume that are not in use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3-getvolumeprotectlevel">GetVolumeProtectLevel</a>
</td>
<td align="left" width="63%">
Gets the shadow copy protection level for the specified volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3-querysnapshotdeltabitmap">QuerySnapshotDeltaBitmap</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3-setvolumeprotectlevel">SetVolumeProtectLevel</a>
</td>
<td align="left" width="63%">
Sets the shadow copy protection level for a volume.

</td>
</tr>
</table> 


## -remarks



An application with administrator privilege can use the <a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3-setvolumeprotectlevel">SetVolumeProtectLevel</a> method to specify a shadow copy protection level for a volume and the separate volume that contains its shadow copy storage area. The same protection level should be set for both volumes. The possible protection levels are defined by the <a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/ne-vsmgmt-vss_protection_level">VSS_PROTECTION_LEVEL</a> enumeration.

When a volume protection fault occurs, the application must call the <a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3-getvolumeprotectlevel">GetVolumeProtectLevel</a> method for the volume to identify the cause of the fault.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt">IVssDifferentialSoftwareSnapshotMgmt</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2">IVssDifferentialSoftwareSnapshotMgmt2</a>
 

 

