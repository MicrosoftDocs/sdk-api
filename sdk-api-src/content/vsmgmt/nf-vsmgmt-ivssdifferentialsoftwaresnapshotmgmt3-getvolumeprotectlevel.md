---
UID: NF:vsmgmt.IVssDifferentialSoftwareSnapshotMgmt3.GetVolumeProtectLevel
title: IVssDifferentialSoftwareSnapshotMgmt3::GetVolumeProtectLevel
author: windows-sdk-content
description: Gets the shadow copy protection level and status for the specified volume.
old-location: base\ivssdifferentialsoftwaresnapshotmgmt3_getvolumeprotectlevel.htm
tech.root: VSS
ms.assetid: a67bf9f1-135b-4881-acd1-6392f27d58e5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetVolumeProtectLevel, GetVolumeProtectLevel method, GetVolumeProtectLevel method,IVssDifferentialSoftwareSnapshotMgmt3 interface, IVssDifferentialSoftwareSnapshotMgmt3 interface,GetVolumeProtectLevel method, IVssDifferentialSoftwareSnapshotMgmt3.GetVolumeProtectLevel, IVssDifferentialSoftwareSnapshotMgmt3::GetVolumeProtectLevel, base.ivssdifferentialsoftwaresnapshotmgmt3_getvolumeprotectlevel, vsmgmt/IVssDifferentialSoftwareSnapshotMgmt3::GetVolumeProtectLevel
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
 - IVssDifferentialSoftwareSnapshotMgmt3.GetVolumeProtectLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssDifferentialSoftwareSnapshotMgmt3::GetVolumeProtectLevel


## -description


Gets the shadow copy protection level and status for the specified volume.


## -parameters




### -param pwszVolumeName [in]

The name of the volume.
      This parameter is required and cannot be <b>NULL</b>.

The name must be in one of the following formats and must include a trailing backslash (\):
       <ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example,   D:\ 
         </li>
<li>A volume GUID path in the form \\?\<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>



### -param protectionLevel [out]

The address of a caller-allocated buffer that receives a <a href="https://msdn.microsoft.com/46cdc46e-fc44-452a-8aae-e47c12deedb4">VSS_VOLUME_PROTECTION_INFO</a> structure containing information about the volume's shadow copy protection level.


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
The shadow copy protection level was queried successfully.

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



The <b>GetVolumeProtectLevel</b> method gets information about the volume's current protection level. If the volume is in a faulted state, the <b>m_protectionFault</b> member of the <a href="https://msdn.microsoft.com/46cdc46e-fc44-452a-8aae-e47c12deedb4">VSS_VOLUME_PROTECTION_INFO</a> structure contains the current protection fault, and the <b>m_failureStatus</b> member contains  the reason why the volume is in a faulted state. If the volume is not in a faulted state, the <b>m_protectionFault</b> and <b>m_failureStatus</b> members will be zero.

If the value of the <i>protectionLevel</i> parameter is <b>VSS_PROTECTION_LEVEL_SNAPSHOT</b>, requesters must set shadow copy storage area (diff area) associations using the <a href="https://msdn.microsoft.com/7b58331c-b8a2-4333-a05d-563395d5f0c2">IVssDifferentialSoftwareSnapshotMgmt::AddDiffArea</a> method.




## -see-also




<a href="https://msdn.microsoft.com/e5abcf69-748a-4ed6-973d-8ba49ec22ef2">IVssDifferentialSoftwareSnapshotMgmt3</a>



<a href="https://msdn.microsoft.com/3f8f3a0c-5076-4ce3-aa8b-5c66ac5fa47a">IVssDifferentialSoftwareSnapshotMgmt3::SetVolumeProtectLevel</a>
 

 

