---
UID: NF:vswriter.IVssCreateWriterMetadata.SetRestoreMethod
title: IVssCreateWriterMetadata::SetRestoreMethod (vswriter.h)
description: The SetRestoreMethod method indicates how the writer's data is to be restored.
helpviewer_keywords: ["IVssCreateWriterMetadata interface [VSS]","SetRestoreMethod method","IVssCreateWriterMetadata.SetRestoreMethod","IVssCreateWriterMetadata::SetRestoreMethod","SetRestoreMethod","SetRestoreMethod method [VSS]","SetRestoreMethod method [VSS]","IVssCreateWriterMetadata interface","_win32_ivsscreatewritermetadata_setrestoremethod","base.ivsscreatewritermetadata_setrestoremethod","vswriter/IVssCreateWriterMetadata::SetRestoreMethod"]
old-location: base\ivsscreatewritermetadata_setrestoremethod.htm
tech.root: base
ms.assetid: 0e04df40-49e4-4f23-b4d5-d6b602162935
ms.date: 12/05/2018
ms.keywords: IVssCreateWriterMetadata interface [VSS],SetRestoreMethod method, IVssCreateWriterMetadata.SetRestoreMethod, IVssCreateWriterMetadata::SetRestoreMethod, SetRestoreMethod, SetRestoreMethod method [VSS], SetRestoreMethod method [VSS],IVssCreateWriterMetadata interface, _win32_ivsscreatewritermetadata_setrestoremethod, base.ivsscreatewritermetadata_setrestoremethod, vswriter/IVssCreateWriterMetadata::SetRestoreMethod
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
 - IVssCreateWriterMetadata::SetRestoreMethod
 - vswriter/IVssCreateWriterMetadata::SetRestoreMethod
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
 - IVssCreateWriterMetadata.SetRestoreMethod
---

# IVssCreateWriterMetadata::SetRestoreMethod


## -description

The 
<b>SetRestoreMethod</b> method indicates how the writer's data is to be restored.

## -parameters

### -param method [in]

<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_restoremethod_enum">VSS_RESTOREMETHOD_ENUM</a> value specifying the method that will be used in the restore operation.

### -param wszService [in]

A pointer to a wide character string containing the name of a service that must be stopped prior to a restore operation and then started after the restore operation takes place, if the value of <i>method</i> is VSS_RME_STOP_RESTORE_START or VSS_RME_RESTORE_STOP_START. 




If the value of <i>method</i> is not VSS_RME_STOP_RESTORE_START or VSS_RME_RESTORE_STOP_START, this argument is not used and should be set to <b>NULL</b>.

### -param wszUserProcedure [in]

Reserved for future use. The value of this parameter should always be set to <b>NULL</b>.

### -param writerRestore [in]

<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_writerrestore_enum">VSS_WRITERRESTORE_ENUM</a> value specifying whether the writer will be involved in restoring its data.

Express writers must set this parameter to <i>VSS_WRE_NEVER</i>.

### -param bRebootRequired [in]

Boolean indicating whether a reboot will be required after the restore operation is complete.

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
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The operation was successful.

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
<dt><b>E_OUTOFMEMORY</b></dt>
<dt>0x8007000EL</dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
<dt>0x80042311L</dt>
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
<dt><b>VSS_E_NOT_SUPPORTED</b></dt>
<dt>0x8004232FL</dt>
</dl>
</td>
<td width="60%">
The caller specified a <a href="/windows/desktop/api/vswriter/ne-vswriter-vss_writerrestore_enum">VSS_WRITERRESTORE_ENUM</a> value that is not supported for express writers.

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

There is a single restore method defined for a writer. If the restore method is not overridden, all of the writer's components will be restored using the same method.

Writers override the restore method on a component-by-component basis by setting a restore target, typically while handling a 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">PreRestore</a> event (<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CVssWriter::OnPreRestore</a>).

It is important to note that despite the fact that restore methods are applied writer-wide, methods are implemented on a per-component basis. For example, if the method specified by the <i>method</i> parameter is VSS_RME_RESTORE_IF_CAN_REPLACE, then all of the files in the component are restored to their original location if they can all be replaced without an error occurring. Otherwise, they are restored to their alternate location if one is specified.

A file should always be restored to its alternate location mapping if either of the following is true:

<ul>
<li>The restore method (set at backup time) is VSS_RME_RESTORE_TO_ALTERNATE_LOCATION.</li>
<li>Its restore target was set (at restore time) to VSS_RT_ALTERNATE.</li>
</ul>
In either case, if no valid alternate location mapping is defined, this constitutes a writer error.

A file can be restored to an alternate location mapping if either of the following is true:

<ul>
<li>The restore method is VSS_RME_RESTORE_IF_NOT_THERE and a version of the file is already present on disk.</li>
<li>The restore method is VSS_RME_RESTORE_IF_CAN_REPLACE and a version of the file is present on disk and cannot be replaced.</li>
</ul>
Again, if no valid alternate location mapping is defined, this constitutes a writer error.

An alternate location mapping is used only during a restore operation and should not be confused with an alternate path, which is used only during a backup operation.

For more information about restore methods, see <a href="/windows/desktop/VSS/setting-vss-restore-methods">Setting VSS Restore Methods</a>.

If the restore method is VSS_RME_STOP_RESTORE_START or VSS_RME_RESTORE_STOP_START, then the correct name of the service must be provided as the <i>wszService</i> argument. For information on writer participation in stopping and restarting services during a restore operation, see <a href="/windows/desktop/VSS/stopping-services-for-restore-by-requestors">Stopping Services for Restore by Requesters</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore">CVssWriter::OnPostRestore</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CVssWriter::OnPreRestore</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscreatewritermetadata">IVssCreateWriterMetadata</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod">IVssExamineWriterMetadata::GetRestoreMethod</a>