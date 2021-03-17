---
UID: NF:vswriter.IVssCreateExpressWriterMetadata.SetRestoreMethod
title: IVssCreateExpressWriterMetadata::SetRestoreMethod (vswriter.h)
description: Specifies how an express writer's data is to be restored.
helpviewer_keywords: ["IVssCreateExpressWriterMetadata interface","SetRestoreMethod method","IVssCreateExpressWriterMetadata.SetRestoreMethod","IVssCreateExpressWriterMetadata::SetRestoreMethod","SetRestoreMethod","SetRestoreMethod method","SetRestoreMethod method","IVssCreateExpressWriterMetadata interface","base.ivsscreateexpresswritermetadata_setrestoremethod","vswriter/IVssCreateExpressWriterMetadata::SetRestoreMethod"]
old-location: base\ivsscreateexpresswritermetadata_setrestoremethod.htm
tech.root: base
ms.assetid: 220e399b-aafd-4b72-bef4-abc3f39f202f
ms.date: 12/05/2018
ms.keywords: IVssCreateExpressWriterMetadata interface,SetRestoreMethod method, IVssCreateExpressWriterMetadata.SetRestoreMethod, IVssCreateExpressWriterMetadata::SetRestoreMethod, SetRestoreMethod, SetRestoreMethod method, SetRestoreMethod method,IVssCreateExpressWriterMetadata interface, base.ivsscreateexpresswritermetadata_setrestoremethod, vswriter/IVssCreateExpressWriterMetadata::SetRestoreMethod
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IVssCreateExpressWriterMetadata::SetRestoreMethod
 - vswriter/IVssCreateExpressWriterMetadata::SetRestoreMethod
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
 - IVssCreateExpressWriterMetadata.SetRestoreMethod
---

# IVssCreateExpressWriterMetadata::SetRestoreMethod


## -description

Specifies how an express writer's data is to be restored.

## -parameters

### -param method [in]

A <a href="/windows/desktop/api/vswriter/ne-vswriter-vss_restoremethod_enum">VSS_RESTOREMETHOD_ENUM</a> enumeration value specifying the restore method to be used in the restore operation. This parameter is required and cannot be <b>VSS_RME_UNDEFINED</b>, <b>VSS_RME_RESTORE_TO_ALTERNATE_LOCATION</b>, or <b>VSS_RME_CUSTOM</b>.

### -param wszService [in]

A pointer to a wide character string containing the name of a service that must be stopped prior to a restore operation and then started after the restore operation takes place, if the value of <i>method</i> is <b>VSS_RME_STOP_RESTORE_START</b> or <b>VSS_RME_RESTORE_STOP_START</b>. 




If the value of <i>method</i> is not <b>VSS_RME_STOP_RESTORE_START</b> or <b>VSS_RME_RESTORE_STOP_START</b>, this parameter is not used and should be set to <b>NULL</b>.

### -param wszUserProcedure [in]

Reserved for future use. The value of this parameter should always be set to <b>NULL</b>.

### -param writerRestore [in]

A <a href="/windows/desktop/api/vswriter/ne-vswriter-vss_writerrestore_enum">VSS_WRITERRESTORE_ENUM</a> enumeration value specifying whether the writer will be involved in restoring its data. This parameter must be set to <b>VSS_WRE_NEVER</b>.

### -param bRebootRequired [in]

A Boolean value indicating whether a reboot will be required after the restore operation is complete.

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
The operation was successful.

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

An express writer can define only one restore method. If the restore method is not overridden, all of the express writer's components will be restored using the same method.

Express writers override the restore method on a component-by-component basis by setting a restore target, typically while handling a 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">PreRestore</a> event (<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CVssWriter::OnPreRestore</a>).

It is important to note that despite the fact that restore methods are applied on a per-writer basis, methods are implemented on a per-component basis. For example, if the method specified by the <i>method</i> parameter is <b>VSS_RME_RESTORE_IF_CAN_REPLACE</b>, then all of the files in the component are restored to their original location if they can all be replaced without an error occurring. Otherwise, they are restored to their alternate location if one is specified.

A file can be restored to an alternate location mapping if either of the following is true:

<ul>
<li>The restore method is <b>VSS_RME_RESTORE_IF_NOT_THERE</b>, and a version of the file is already present on disk.</li>
<li>The restore method is <b>VSS_RME_RESTORE_IF_CAN_REPLACE</b>, and a version of the file is present on disk and cannot be replaced.</li>
</ul>
If no valid alternate location mapping is defined, this is a writer error.

For more information about restore methods, see <a href="/windows/desktop/VSS/setting-vss-restore-methods">Setting VSS Restore Methods</a>.

If the restore method is VSS_RME_STOP_RESTORE_START or VSS_RME_RESTORE_STOP_START, then the correct name of the service must be provided as the <i>wszService</i> argument. For information on writer participation in stopping and restarting services during a restore operation, see <a href="/windows/desktop/VSS/stopping-services-for-restore-by-requestors">Stopping Services for Restore by Requesters</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscreateexpresswritermetadata">IVssCreateExpressWriterMetadata</a>