---
UID: NF:vswriter.IVssComponentEx2.SetFailure
title: IVssComponentEx2::SetFailure (vswriter.h)
description: VSS writers call this method to report errors at the component level.
helpviewer_keywords: ["IVssComponentEx2 interface","SetFailure method","IVssComponentEx2.SetFailure","IVssComponentEx2::SetFailure","S_OK","SetFailure","SetFailure method","SetFailure method","IVssComponentEx2 interface","VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT","VSS_E_WRITERERROR_NONRETRYABLE","VSS_E_WRITERERROR_OUTOFRESOURCES","VSS_E_WRITERERROR_RETRYABLE","VSS_E_WRITERERROR_TIMEOUT","base.ivsscomponentex2_setfailure","vswriter/IVssComponentEx2::SetFailure"]
old-location: base\ivsscomponentex2_setfailure.htm
tech.root: base
ms.assetid: f9fd728a-b205-4cfa-8e9e-e0a0d385f5a1
ms.date: 12/05/2018
ms.keywords: IVssComponentEx2 interface,SetFailure method, IVssComponentEx2.SetFailure, IVssComponentEx2::SetFailure, S_OK, SetFailure, SetFailure method, SetFailure method,IVssComponentEx2 interface, VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT, VSS_E_WRITERERROR_NONRETRYABLE, VSS_E_WRITERERROR_OUTOFRESOURCES, VSS_E_WRITERERROR_RETRYABLE, VSS_E_WRITERERROR_TIMEOUT, base.ivsscomponentex2_setfailure, vswriter/IVssComponentEx2::SetFailure
req.header: vswriter.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssComponentEx2::SetFailure
 - vswriter/IVssComponentEx2::SetFailure
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - vswriter.h
api_name:
 - IVssComponentEx2.SetFailure
---

# IVssComponentEx2::SetFailure


## -description

VSS writers call this method to report errors at the component level.

## -parameters

### -param hr [in]

The error code to be returned to the requester that calls the <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex2-getfailure">IVssComponentEx2::GetFailure</a> method. 
      

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
</table>

### -param hrApplication [in]

An additional error code to be returned to the requester. This parameter is optional.

### -param wszApplicationMessage [in]

A string containing an error message for the requester  to display to the end user. The writer is responsible for localizing this string if necessary before using it in this method. This parameter is optional and can be <b>NULL</b> or an empty string.

### -param dwReserved [in]

This parameter is reserved for future use and should be set to zero.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In addition to calling this method,  use the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-setwriterfailureex">CVssWriterEx2::SetWriterFailureEx</a> method to report that a partial writer failure has occurred.

This method cannot be called from <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onidentify">CVssWriter::OnIdentify</a> or <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex-onidentifyex">CVssWriterEx::OnIdentifyEx</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponentex2">IVssComponentEx2</a>