---
UID: NF:vsmgmt.IVssDifferentialSoftwareSnapshotMgmt3.DeleteUnusedDiffAreas
title: IVssDifferentialSoftwareSnapshotMgmt3::DeleteUnusedDiffAreas
author: windows-sdk-content
description: Deletes all shadow copy storage areas (also called diff areas) on the specified volume that are not in use.
old-location: base\ivssdifferentialsoftwaresnapshotmgmt3_deleteunuseddiffareas.htm
old-project: VSS
ms.assetid: daa23f2c-8342-4387-800a-def5951896ee
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: DeleteUnusedDiffAreas, DeleteUnusedDiffAreas method, DeleteUnusedDiffAreas method,IVssDifferentialSoftwareSnapshotMgmt3 interface, IVssDifferentialSoftwareSnapshotMgmt3 interface,DeleteUnusedDiffAreas method, IVssDifferentialSoftwareSnapshotMgmt3.DeleteUnusedDiffAreas, IVssDifferentialSoftwareSnapshotMgmt3::DeleteUnusedDiffAreas, base.ivssdifferentialsoftwaresnapshotmgmt3_deleteunuseddiffareas, vsmgmt/IVssDifferentialSoftwareSnapshotMgmt3::DeleteUnusedDiffAreas
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
 - IVssDifferentialSoftwareSnapshotMgmt3.DeleteUnusedDiffAreas
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssDifferentialSoftwareSnapshotMgmt3::DeleteUnusedDiffAreas


## -description


Deletes all shadow copy storage areas (also called diff areas) on the specified  volume that are not in use.


## -parameters




### -param pwszDiffAreaVolumeName [in]

The name of the volume.
      This parameter is required and cannot be <b>NULL</b>.

The name must be in one of the following formats and must include a trailing backslash (\):
       <ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example,  D:\ 
         </li>
<li>A volume GUID path in the form \\?\<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>



## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The shadow copy storage areas were successfully deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
<dt>0x80070005L</dt>
</dl>
</td>
<td width="60%">
The caller is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057L</dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
<dt>0x80000001L</dt>
</dl>
</td>
<td width="60%">
The provider for the volume does not support shadow copy protection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
<dt>0x80042306L</dt>
</dl>
</td>
<td width="60%">
An expected provider error has occurred. The error code is logged in the event log. For more information, see <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042308L</dt>
</dl>
</td>
<td width="60%">
The specified volume was not found.

</td>
</tr>
</table>
 




## -remarks



Unused shadow copy storage area files are found on storage area volumes when the associated original volume is offline due to a protection fault. In certain cases, the original volume may be permanently lost, and calling the <b>DeleteUnusedDiffAreas</b> method is the only way to recover the abandoned storage area space.




## -see-also




<a href="https://msdn.microsoft.com/e5abcf69-748a-4ed6-973d-8ba49ec22ef2">IVssDifferentialSoftwareSnapshotMgmt3</a>
 

 

