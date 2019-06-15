---
UID: NF:vsmgmt.IVssDifferentialSoftwareSnapshotMgmt.QueryVolumesSupportedForDiffAreas
title: IVssDifferentialSoftwareSnapshotMgmt::QueryVolumesSupportedForDiffAreas (vsmgmt.h)
author: windows-sdk-content
description: Queries volumes that support shadow copy storage areas (including volumes with disabled shadow copy storage areas).
old-location: base\ivssdifferentialsoftwaresnapshotmgmt_queryvolumessupportedfordiffareas.htm
tech.root: VSS
ms.assetid: 2aad75e3-0228-4cc4-b813-c70a7ebfdea5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVssDifferentialSoftwareSnapshotMgmt interface [VSS],QueryVolumesSupportedForDiffAreas method, IVssDifferentialSoftwareSnapshotMgmt.QueryVolumesSupportedForDiffAreas, IVssDifferentialSoftwareSnapshotMgmt::QueryVolumesSupportedForDiffAreas, QueryVolumesSupportedForDiffAreas, QueryVolumesSupportedForDiffAreas method [VSS], QueryVolumesSupportedForDiffAreas method [VSS],IVssDifferentialSoftwareSnapshotMgmt interface, base.ivssdifferentialsoftwaresnapshotmgmt_queryvolumessupportedfordiffareas, vsmgmt/IVssDifferentialSoftwareSnapshotMgmt::QueryVolumesSupportedForDiffAreas
ms.topic: method
f1_keywords: ["vsmgmt/IVssDifferentialSoftwareSnapshotMgmt.QueryVolumesSupportedForDiffAreas"]
req.header: vsmgmt.h
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
 - IVssDifferentialSoftwareSnapshotMgmt.QueryVolumesSupportedForDiffAreas
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssDifferentialSoftwareSnapshotMgmt::QueryVolumesSupportedForDiffAreas


## -description


The 
    <b>QueryVolumesSupportedForDiffAreas</b> 
    method queries volumes that support shadow copy storage areas (including volumes with disabled 
    shadow copy storage areas).


## -parameters




### -param pwszOriginalVolumeName [in]

Name of the original volume that is the source of the shadow copies. The name of the volume must be in one 
      of the following formats and must include a trailing backslash (\):
      

<ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, 
        D:\</li>
<li>A volume GUID path of the form \\?\<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>

### -param ppEnum [out]

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssenummgmtobject">IVssEnumMgmtObject</a> interface 
      pointer, which is initialized on return. Callers must release the interface.


## -returns



This method can return one of these values.

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
Successfully queried the shadow copy storage area volumes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Caller does not have sufficient backup privileges or is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">
Provider error - the provider logged the error in the event log. For more information, see 
        <a href="https://docs.microsoft.com/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="https://docs.microsoft.com/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>
 




## -remarks



The returned <a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssenummgmtobject">IVssEnumMgmtObject</a> enumerator object 
    will contain <a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/ns-vsmgmt-_vss_diff_volume_prop">VSS_DIFF_VOLUME_PROP</a> structures inside 
    the <a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001">VSS_MGMT_OBJECT_UNION</a> union inside the 
    <a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/ns-vsmgmt-_vss_mgmt_object_prop">VSS_MGMT_OBJECT_PROP</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt">IVssDifferentialSoftwareSnapshotMgmt</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssenummgmtobject">IVssEnumMgmtObject</a>
 

 

