---
UID: NF:vsbackup.IVssBackupComponents.SetAdditionalRestores
title: IVssBackupComponents::SetAdditionalRestores (vsbackup.h)
description: The SetAdditionalRestores method is used by a requester during incremental or differential restore operations to indicate to writers that a given component will require additional restore operations to completely retrieve it.
helpviewer_keywords: ["IVssBackupComponents interface [VSS]","SetAdditionalRestores method","IVssBackupComponents.SetAdditionalRestores","IVssBackupComponents::SetAdditionalRestores","SetAdditionalRestores","SetAdditionalRestores method [VSS]","SetAdditionalRestores method [VSS]","IVssBackupComponents interface","_win32_ivssbackupcomponents_setadditionalrestores","base.ivssbackupcomponents_setadditionalrestores","vsbackup/IVssBackupComponents::SetAdditionalRestores"]
old-location: base\ivssbackupcomponents_setadditionalrestores.htm
tech.root: base
ms.assetid: b3a38348-ab89-40a5-bf77-612bcd99c31b
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents interface [VSS],SetAdditionalRestores method, IVssBackupComponents.SetAdditionalRestores, IVssBackupComponents::SetAdditionalRestores, SetAdditionalRestores, SetAdditionalRestores method [VSS], SetAdditionalRestores method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_setadditionalrestores, base.ivssbackupcomponents_setadditionalrestores, vsbackup/IVssBackupComponents::SetAdditionalRestores
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
 - IVssBackupComponents::SetAdditionalRestores
 - vsbackup/IVssBackupComponents::SetAdditionalRestores
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
 - IVssBackupComponents.SetAdditionalRestores
---

# IVssBackupComponents::SetAdditionalRestores


## -description

The 
<b>SetAdditionalRestores</b> method is used by a requester during incremental or differential restore operations to indicate to writers that a given component will require additional restore operations to completely retrieve it.

## -parameters

### -param writerId [in]

Writer identifier.

### -param ct [in]

Type of the component. See 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a> for the possible values.

### -param wszLogicalPath [in]

<b>Null</b>-terminated wide character string containing the logical path of the component to be added. 


For more information, see <a href="/windows/desktop/VSS/logical-pathing-of-components">Logical Pathing of Components</a>.

The value of the string containing the logical path used here should be the same as was used when the component was added to the backup set using 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>.

The logical path can be <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.

### -param wszComponentName [in]

<b>Null</b>-terminated wide character string containing the name of the component. 




The value of the string should not be <b>NULL</b>, and should contain the same component as was used when the component was added to the backup set using 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>.

### -param bAdditionalRestores [in]

If the value of this parameter is <b>true</b>, additional restores of the component will follow this restore. If the value is <b>false</b>, additional restores of the component will not follow this restore.

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
Successfully set the additional restore status.

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
The backup components object is not initialized, this method has been called during a restore operation, or this method has not been called within the correct sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The backup component does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more information, see 
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
</table>

## -remarks

The information provided by the 
<b>SetAdditionalRestores</b> method is typically used by writers that support an explicit recovery mechanism as part of their 
PostRestore event handler (<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore">CVssWriter::OnPostRestore</a>)—for instance, the Exchange Server, and database applications such as SQL Server. For these applications, it is often not possible to perform additional differential, incremental, or log restores after such a recovery is performed.

Therefore, if 
<b>SetAdditionalRestores</b> for a component is set to <b>true</b>, this means that such a writer should not execute its explicit recovery mechanism and should expect that additional differential, incremental, or log restores will be done.

When 
<b>SetAdditionalRestores</b> on a component is set to <b>false</b>, then after the component is restored, the application can complete its recovery operation and be brought back online.

This method must be called before 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a>