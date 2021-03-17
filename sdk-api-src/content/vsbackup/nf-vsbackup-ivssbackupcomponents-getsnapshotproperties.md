---
UID: NF:vsbackup.IVssBackupComponents.GetSnapshotProperties
title: IVssBackupComponents::GetSnapshotProperties (vsbackup.h)
description: The GetSnapshotProperties method gets the properties of the specified shadow copy.
helpviewer_keywords: ["GetSnapshotProperties","GetSnapshotProperties method [VSS]","GetSnapshotProperties method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","GetSnapshotProperties method","IVssBackupComponents.GetSnapshotProperties","IVssBackupComponents::GetSnapshotProperties","_win32_ivssbackupcomponents_getsnapshotproperties","base.ivssbackupcomponents_getsnapshotproperties","vsbackup/IVssBackupComponents::GetSnapshotProperties"]
old-location: base\ivssbackupcomponents_getsnapshotproperties.htm
tech.root: base
ms.assetid: a4e2f9f3-7dee-4324-a48a-6de2a32eabf7
ms.date: 12/05/2018
ms.keywords: GetSnapshotProperties, GetSnapshotProperties method [VSS], GetSnapshotProperties method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],GetSnapshotProperties method, IVssBackupComponents.GetSnapshotProperties, IVssBackupComponents::GetSnapshotProperties, _win32_ivssbackupcomponents_getsnapshotproperties, base.ivssbackupcomponents_getsnapshotproperties, vsbackup/IVssBackupComponents::GetSnapshotProperties
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssBackupComponents::GetSnapshotProperties
 - vsbackup/IVssBackupComponents::GetSnapshotProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssBackupComponents.GetSnapshotProperties
---

# IVssBackupComponents::GetSnapshotProperties


## -description

The <b>GetSnapshotProperties</b> 
    method gets the properties of the specified shadow copy.

## -parameters

### -param SnapshotId [in]

The identifier of the shadow copy of a volume as returned by 
      <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset">IVssBackupComponents::AddToSnapshotSet</a>.

### -param pProp [out]

The address of a caller-allocated <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure that receives 
      the shadow copy properties.
      The software provider is responsible for setting the members of this structure. The software provider allocates memory for all string members  that it sets in the structure. When the structure is no longer needed, the software provider is responsible for freeing these strings by calling the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-vssfreesnapshotproperties">VssFreeSnapshotProperties</a> function.

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
Successfully returned the shadow copy properties.

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
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
The backup components object is not initialized, this method has been called during a restore operation, or 
        this method has not been called within the correct sequence.
       

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
Expected provider error. The provider logged the error in the event log. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.
       

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
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED_PROVIDER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Unexpected provider error. The error code is logged in the error log. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event 
        and Error Handling Under VSS</a>.
       

</td>
</tr>
</table>

## -remarks

The caller should set the contents of the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure to zero before calling the <b>GetSnapshotProperties</b> method.

The provider is responsible for allocating and freeing the strings in the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset">IVssBackupComponents::AddToSnapshotSet</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset">IVssBackupComponents::StartSnapshotSet</a>



<a href="/windows/desktop/VSS/volume-shadow-copy-api-data-types">VSS_ID</a>



<a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-vssfreesnapshotproperties">VssFreeSnapshotProperties</a>