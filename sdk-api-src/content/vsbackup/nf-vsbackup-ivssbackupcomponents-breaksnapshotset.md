---
UID: NF:vsbackup.IVssBackupComponents.BreakSnapshotSet
title: IVssBackupComponents::BreakSnapshotSet
author: windows-sdk-content
description: The BreakSnapshotSet method causes the existence of a shadow copy set to be &#0034;forgotten&#0034; by VSS.
old-location: base\ivssbackupcomponents_breaksnapshotset.htm
old-project: VSS
ms.assetid: 8c366f19-b10f-46cd-b5dc-cc3c77c5a008
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: BreakSnapshotSet, BreakSnapshotSet method [VSS], BreakSnapshotSet method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],BreakSnapshotSet method, IVssBackupComponents.BreakSnapshotSet, IVssBackupComponents::BreakSnapshotSet, _win32_ivssbackupcomponents_breaksnapshotset, base.ivssbackupcomponents_breaksnapshotset, vsbackup/IVssBackupComponents::BreakSnapshotSet
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: AMVPSIZE, *LPAMVPSIZE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssBackupComponents.BreakSnapshotSet
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssBackupComponents::BreakSnapshotSet


## -description


The 
<b>BreakSnapshotSet</b> method causes the existence of a shadow copy set to be "forgotten" by VSS.


## -parameters




### -param SnapshotSetId [in]

Shadow copy set identifier.


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
The shadow copy set was successfully broken.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient backup privileges or is not an administrator.

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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified shadow copy does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">
The shadow copy was created by a software provider and cannot be broken.

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
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>
 




## -remarks



<b>BreakSnapshotSet</b> can be used only for shadow copies created by a hardware shadow copy provider. This method makes these shadow copies regular volumes.

Shadow copies of volumes "broken" with 
<b>BreakSnapshotSet</b> must be managed independently of VSS as stand-alone volumes. See 
<a href="https://msdn.microsoft.com/fb796b2f-b6fb-48ee-8d42-36f88cb165aa">Breaking Shadow Copies</a> for more information.


<a href="https://msdn.microsoft.com/595fe295-082d-4130-9698-952df49a922e">IVssBackupComponentsEx2::BreakSnapshotSetEx</a> is similar to the <b>BreakSnapshotSet</b> method, except that it has extra parameters to query status and specify how the shadow copy set is broken.




## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/2e06f69e-8210-4773-8080-5c58e6f59792">IVssBackupComponents::DeleteSnapshots</a>
 

 

