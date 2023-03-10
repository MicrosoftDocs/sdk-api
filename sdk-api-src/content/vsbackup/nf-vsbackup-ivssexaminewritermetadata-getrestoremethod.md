---
UID: NF:vsbackup.IVssExamineWriterMetadata.GetRestoreMethod
title: IVssExamineWriterMetadata::GetRestoreMethod (vsbackup.h)
description: The GetRestoreMethod method returns information about how a writer wants its data to be restored.
helpviewer_keywords: ["GetRestoreMethod","GetRestoreMethod method [VSS]","GetRestoreMethod method [VSS]","IVssExamineWriterMetadata interface","IVssExamineWriterMetadata interface [VSS]","GetRestoreMethod method","IVssExamineWriterMetadata.GetRestoreMethod","IVssExamineWriterMetadata::GetRestoreMethod","_win32_ivssexaminewritermetadata_getrestoremethod","base.ivssexaminewritermetadata_getrestoremethod","vsbackup/IVssExamineWriterMetadata::GetRestoreMethod"]
old-location: base\ivssexaminewritermetadata_getrestoremethod.htm
tech.root: base
ms.assetid: c93f841f-057c-4aee-b8f2-263395e84c7b
ms.date: 12/05/2018
ms.keywords: GetRestoreMethod, GetRestoreMethod method [VSS], GetRestoreMethod method [VSS],IVssExamineWriterMetadata interface, IVssExamineWriterMetadata interface [VSS],GetRestoreMethod method, IVssExamineWriterMetadata.GetRestoreMethod, IVssExamineWriterMetadata::GetRestoreMethod, _win32_ivssexaminewritermetadata_getrestoremethod, base.ivssexaminewritermetadata_getrestoremethod, vsbackup/IVssExamineWriterMetadata::GetRestoreMethod
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
 - IVssExamineWriterMetadata::GetRestoreMethod
 - vsbackup/IVssExamineWriterMetadata::GetRestoreMethod
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
 - IVssExamineWriterMetadata.GetRestoreMethod
---

# IVssExamineWriterMetadata::GetRestoreMethod


## -description

The 
<b>GetRestoreMethod</b> method returns information about how a writer wants its data to be restored.

## -parameters

### -param pMethod [out]

Pointer to a 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_restoremethod_enum">VSS_RESTOREMETHOD_ENUM</a> value that specifies file overwriting, the use of alternate locations specifying the method that will be used in the restore operation.

### -param pbstrService [out]

If the value of <i>pMethod</i> is VSS_RME_STOP_RESTORE_START or VSS_RME_RESTORE_STOP_START, a pointer to a string containing the name of the service that is started and stopped. Otherwise, the value is <b>NULL</b>.

### -param pbstrUserProcedure [out]

Pointer to the URL of an HTML or XML document describing to the user how the restore is to be performed. The value may be <b>NULL</b>.

### -param pwriterRestore [out]

Pointer to a 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_writerrestore_enum">VSS_WRITERRESTORE_ENUM</a> value specifying whether the writer will be involved in restoring its data.

### -param pbRebootRequired [out]

Pointer to a Boolean value indicating whether a reboot will be required after the restore operation is complete. The value receives <b>true</b>  if a reboot will be required, or  <b>false</b> otherwise.

### -param pcMappings [out]

Pointer to the number of alternate mappings associated with the writer.

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
Successfully returned the restore method information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
A restore method does not exist.

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

The caller must free the memory used by the <i>pbstrUserProcedure</i> and <i>pbstrService</i> parameters by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

A file should always be restored to its alternate location mapping if either of the following is true:

<ul>
<li>The restore method (set at backup time) is VSS_RME_RESTORE_TO_ALTERNATE_LOCATION.</li>
<li>Its restore target was set (at restore time) to VSS_RT_ALTERNATE.</li>
</ul>
In either case, if no valid alternate location mapping is defined, this constitutes a writer error.

A file can be restored to an alternate location mapping if :

<ul>
<li>The restore method is VSS_RME_RESTORE_IF_NOT_THERE and a version of the file is already present on disk.</li>
<li>The restore method is VSS_RME_RESTORE_IF_CAN_REPLACE and a version of the file is present on disk and cannot be replaced.</li>
</ul>
Again, if no valid alternate location mapping is defined, this constitutes a writer error.

An alternate location mapping is used only during a restore operation and should not be confused with an alternate path, which is used only during a backup operation.

For more information about restore methods, see <a href="/windows/desktop/VSS/setting-vss-restore-methods">Setting VSS Restore Methods</a>.

If the restore method is VSS_RME_STOP_RESTORE_START or VSS_RME_RESTORE_STOP_START, a requester uses the name returned by <i>pbstrService</i> to determine which service must be stopped during and then restarted after restore. See 
<a href="/windows/desktop/VSS/stopping-services-for-restore-by-requestors">Stopping Services For Restore by Requesters</a> for information on writer participation in stopping and restarting services during a restore operation.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod">IVssCreateWriterMetadata::SetRestoreMethod</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a>