---
UID: NF:vswriter.CVssWriterEx2.SetWriterFailureEx
title: CVssWriterEx2::SetWriterFailureEx (vswriter.h)
description: Sets extended error information to indicate that the writer has encountered a problem with participating in a VSS operation.
helpviewer_keywords: ["CVssWriterEx2 interface","SetWriterFailureEx method","CVssWriterEx2.SetWriterFailureEx","CVssWriterEx2::SetWriterFailureEx","S_OK","SetWriterFailureEx","SetWriterFailureEx method","SetWriterFailureEx method","CVssWriterEx2 interface","VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT","VSS_E_WRITERERROR_NONRETRYABLE","VSS_E_WRITERERROR_OUTOFRESOURCES","VSS_E_WRITERERROR_PARTIAL_FAILURE","VSS_E_WRITERERROR_RETRYABLE","VSS_E_WRITERERROR_TIMEOUT","base.cvsswriterex2_setwriterfailureex","vswriter/CVssWriterEx2::SetWriterFailureEx"]
old-location: base\cvsswriterex2_setwriterfailureex.htm
tech.root: base
ms.assetid: c049a016-6546-4e72-90e8-46be8c2f7764
ms.date: 12/05/2018
ms.keywords: CVssWriterEx2 interface,SetWriterFailureEx method, CVssWriterEx2.SetWriterFailureEx, CVssWriterEx2::SetWriterFailureEx, S_OK, SetWriterFailureEx, SetWriterFailureEx method, SetWriterFailureEx method,CVssWriterEx2 interface, VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT, VSS_E_WRITERERROR_NONRETRYABLE, VSS_E_WRITERERROR_OUTOFRESOURCES, VSS_E_WRITERERROR_PARTIAL_FAILURE, VSS_E_WRITERERROR_RETRYABLE, VSS_E_WRITERERROR_TIMEOUT, base.cvsswriterex2_setwriterfailureex, vswriter/CVssWriterEx2::SetWriterFailureEx
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
 - CVssWriterEx2::SetWriterFailureEx
 - vswriter/CVssWriterEx2::SetWriterFailureEx
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
 - CVssWriterEx2.SetWriterFailureEx
---

# CVssWriterEx2::SetWriterFailureEx


## -description

Sets extended error information to indicate that the writer has encountered a problem with participating in a VSS 
       operation.

## -parameters

### -param hrWriter [in]

The error code to be returned to the requester. 
      

The following are the error codes that this method can set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="S_OK"></a><a id="s_ok"></a><dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The writer was successful.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT"></a><a id="vss_e_writererror_inconsistentsnapshot"></a><dl>
<dt><b>VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT</b></dt>
</dl>
</td>
<td width="60%">
The shadow copy contains only a subset of the volumes needed by the writer to correctly back up the 
        application component.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_OUTOFRESOURCES"></a><a id="vss_e_writererror_outofresources"></a><dl>
<dt><b>VSS_E_WRITERERROR_OUTOFRESOURCES</b></dt>
</dl>
</td>
<td width="60%">
The writer ran out of memory or other system resources. The recommended way to handle this error code is 
        to wait ten minutes and then repeat the operation, up to three times.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_TIMEOUT"></a><a id="vss_e_writererror_timeout"></a><dl>
<dt><b>VSS_E_WRITERERROR_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The writer operation failed because of a time-out between the Freeze and Thaw events. The recommended way 
        to handle this error code is to wait ten minutes and then repeat the operation, up to three times.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_RETRYABLE"></a><a id="vss_e_writererror_retryable"></a><dl>
<dt><b>VSS_E_WRITERERROR_RETRYABLE</b></dt>
</dl>
</td>
<td width="60%">
The writer failed due to an error that would likely not occur if the entire backup, restore, or shadow 
        copy creation process was restarted. The recommended way to handle this error code is to wait ten minutes and 
        then repeat the operation, up to three times.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_NONRETRYABLE"></a><a id="vss_e_writererror_nonretryable"></a><dl>
<dt><b>VSS_E_WRITERERROR_NONRETRYABLE</b></dt>
</dl>
</td>
<td width="60%">
The writer operation failed because of an error that might recur if another shadow copy is created. For 
        more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_PARTIAL_FAILURE"></a><a id="vss_e_writererror_partial_failure"></a><dl>
<dt><b>VSS_E_WRITERERROR_PARTIAL_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The writer is reporting one or more component-level errors. To report the errors, the writer must use the <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex2-setfailure">IVssComponentEx2::SetFailure</a> method.

</td>
</tr>
</table>

### -param hrApplication [in]

An additional error code to be returned to the requester. This parameter is optional.

### -param wszApplicationMessage [in]

A string containing an error message for the requester  to display to the end user. The writer is responsible for localizing this string if necessary before using it in this method. This parameter is optional and can be <b>NULL</b> or an empty string.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method cannot be called from <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onidentify">CVssWriter::OnIdentify</a> or <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex-onidentifyex">CVssWriterEx::OnIdentifyEx</a>.

To report component-level errors, writers should use the <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex2-setfailure">IVssComponentEx2::SetFailure</a> method.

If a writer's event handler (such as <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onfreeze">CVssWriter::OnFreeze</a>) calls this method, it must do so in the same thread that called the event handler. For more information, see 
<a href="/windows/desktop/VSS/writers">Writer Event Handling</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriterex2">CVssWriterEx2</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex3-getwriterstatusex">IVssBackupComponentsEx3::GetWriterStatusEx</a>