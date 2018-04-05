---
UID: NF:vsmgmt.IVssDifferentialSoftwareSnapshotMgmt3.ClearVolumeProtectFault
title: IVssDifferentialSoftwareSnapshotMgmt3::ClearVolumeProtectFault method
author: windows-driver-content
description: Clears the protection fault state for the specified volume.
old-location: base\ivssdifferentialsoftwaresnapshotmgmt3_clearvolumeprotectfault.htm
old-project: VSS
ms.assetid: 07257d34-23b1-47bf-b613-f65f5d2a977e
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ClearVolumeProtectFault method, ClearVolumeProtectFault method, IVssDifferentialSoftwareSnapshotMgmt3 interface, ClearVolumeProtectFault,IVssDifferentialSoftwareSnapshotMgmt3.ClearVolumeProtectFault, IVssDifferentialSoftwareSnapshotMgmt3, IVssDifferentialSoftwareSnapshotMgmt3 interface, ClearVolumeProtectFault method, IVssDifferentialSoftwareSnapshotMgmt3::ClearVolumeProtectFault, base.ivssdifferentialsoftwaresnapshotmgmt3_clearvolumeprotectfault, vsmgmt/IVssDifferentialSoftwareSnapshotMgmt3::ClearVolumeProtectFault
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: VSS_PROTECTION_LEVEL, *PVSS_PROTECTION_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VsMgmt.h
api_name:
-	IVssDifferentialSoftwareSnapshotMgmt3.ClearVolumeProtectFault
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssDifferentialSoftwareSnapshotMgmt3::ClearVolumeProtectFault method


## -description


Clears the protection fault state for the specified volume.


## -parameters




### -param pwszVolumeName [in]

The name of the volume.
      This parameter is required and cannot be <b>NULL</b>.

The name must be in one of the following formats and must include a trailing backslash (\):
       <ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, D:\ 
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
The protection fault state was cleared successfully.

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



The <b>ClearVolumeProtectFault</b> method dismounts the volume and resets the volume's protection fault member to <b>FALSE</b> to allow normal I/O to continue on the volume. If the volume is not in a faulted state, this method does nothing.




## -see-also




<a href="https://msdn.microsoft.com/e5abcf69-748a-4ed6-973d-8ba49ec22ef2">IVssDifferentialSoftwareSnapshotMgmt3</a>
 

 

