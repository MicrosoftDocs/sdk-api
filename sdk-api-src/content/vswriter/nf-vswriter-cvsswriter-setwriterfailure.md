---
UID: NF:vswriter.CVssWriter.SetWriterFailure
title: CVssWriter::SetWriterFailure (vswriter.h)
description: The SetWriterFailure method indicates that this writer has encountered an error condition and sets an error condition.
helpviewer_keywords: ["CVssWriter interface [VSS]","SetWriterFailure method","CVssWriter.SetWriterFailure","CVssWriter::SetWriterFailure","SetWriterFailure","SetWriterFailure method [VSS]","SetWriterFailure method [VSS]","CVssWriter interface","VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT","VSS_E_WRITERERROR_NONRETRYABLE","VSS_E_WRITERERROR_OUTOFRESOURCES","VSS_E_WRITERERROR_RETRYABLE","VSS_E_WRITERERROR_TIMEOUT","_win32_cvsswriter_setwriterfailure","base.cvsswriter_setwriterfailure","vswriter/CVssWriter::SetWriterFailure"]
old-location: base\cvsswriter_setwriterfailure.htm
tech.root: base
ms.assetid: 9fef9d77-dc0d-4ba0-a317-5c62355458f7
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],SetWriterFailure method, CVssWriter.SetWriterFailure, CVssWriter::SetWriterFailure, SetWriterFailure, SetWriterFailure method [VSS], SetWriterFailure method [VSS],CVssWriter interface, VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT, VSS_E_WRITERERROR_NONRETRYABLE, VSS_E_WRITERERROR_OUTOFRESOURCES, VSS_E_WRITERERROR_RETRYABLE, VSS_E_WRITERERROR_TIMEOUT, _win32_cvsswriter_setwriterfailure, base.cvsswriter_setwriterfailure, vswriter/CVssWriter::SetWriterFailure
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
 - CVssWriter::SetWriterFailure
 - vswriter/CVssWriter::SetWriterFailure
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
 - CVssWriter.SetWriterFailure
---

# CVssWriter::SetWriterFailure


## -description

The 
<b>SetWriterFailure</b> method indicates that this writer has encountered an error condition and sets an error condition.

<b>SetWriterFailure</b> is a protected method implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class.

## -parameters

### -param hr [in]

Error code to be set. The following are the error codes that this method can set. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT"></a><a id="vss_e_writererror_inconsistentsnapshot"></a><dl>
<dt><b>VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT</b></dt>
</dl>
</td>
<td width="60%">
The shadow copy contains only a subset of the volumes needed to correctly back up an application component.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_NONRETRYABLE"></a><a id="vss_e_writererror_nonretryable"></a><dl>
<dt><b>VSS_E_WRITERERROR_NONRETRYABLE</b></dt>
</dl>
</td>
<td width="60%">
The writer failed due to an error that would likely occur if another shadow copy is created.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_OUTOFRESOURCES"></a><a id="vss_e_writererror_outofresources"></a><dl>
<dt><b>VSS_E_WRITERERROR_OUTOFRESOURCES</b></dt>
</dl>
</td>
<td width="60%">
The writer failed due to a resource allocation error.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_RETRYABLE"></a><a id="vss_e_writererror_retryable"></a><dl>
<dt><b>VSS_E_WRITERERROR_RETRYABLE</b></dt>
</dl>
</td>
<td width="60%">
The writer failed due to an error that would likely not occur if the entire backup, restore, or shadow copy creation process was restarted.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_TIMEOUT"></a><a id="vss_e_writererror_timeout"></a><dl>
<dt><b>VSS_E_WRITERERROR_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The writer could not complete the shadow copy creation because the time between freeze and thaw states exceeded the time-out value (<i>dwTimeoutFreeze</i>) set in 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">CVssWriter::Initialize</a>.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method cannot be called from <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onidentify">CVssWriter::OnIdentify</a> or <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex-onidentifyex">CVssWriterEx::OnIdentifyEx</a>.

If a writer's event handler (such as <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onfreeze">CVssWriter::OnFreeze</a>) calls this method, it must do so in the same thread that called the event handler. For more information, see 
<a href="/windows/desktop/VSS/writers">Writer Event Handling</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus">IVssBackupComponents::GetWriterStatus</a>