---
UID: NF:vswriter.CVssWriterEx2.SetWriterFailureEx
title: CVssWriterEx2::SetWriterFailureEx
author: windows-sdk-content
description: Sets extended error information to indicate that the writer has encountered a problem with participating in a VSS operation.
old-location: base\cvsswriterex2_setwriterfailureex.htm
old-project: VSS
ms.assetid: c049a016-6546-4e72-90e8-46be8c2f7764
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: CVssWriterEx2 interface,SetWriterFailureEx method, CVssWriterEx2.SetWriterFailureEx, CVssWriterEx2::SetWriterFailureEx, S_OK, SetWriterFailureEx, SetWriterFailureEx method, SetWriterFailureEx method,CVssWriterEx2 interface, VSS_E_WRITERERROR_INCONSISTENTSNAPSHOT, VSS_E_WRITERERROR_NONRETRYABLE, VSS_E_WRITERERROR_OUTOFRESOURCES, VSS_E_WRITERERROR_PARTIAL_FAILURE, VSS_E_WRITERERROR_RETRYABLE, VSS_E_WRITERERROR_TIMEOUT, base.cvsswriterex2_setwriterfailureex, vswriter/CVssWriterEx2::SetWriterFailureEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	CVssWriterEx2.SetWriterFailureEx
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
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
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_E_WRITERERROR_PARTIAL_FAILURE"></a><a id="vss_e_writererror_partial_failure"></a><dl>
<dt><b>VSS_E_WRITERERROR_PARTIAL_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The writer is reporting one or more component-level errors. To report the errors, the writer must use the <a href="https://msdn.microsoft.com/f9fd728a-b205-4cfa-8e9e-e0a0d385f5a1">IVssComponentEx2::SetFailure</a> method.

</td>
</tr>
</table>
 


### -param hrApplication [in]

An additional error code to be returned to the requester. This parameter is optional.


### -param wszApplicationMessage [in]

A string containing an error message for the requester  to display to the end user. The writer is responsible for localizing this string if necessary before using it in this method. This parameter is optional and can be <b>NULL</b> or an empty string.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method cannot be called from <a href="https://msdn.microsoft.com/542d479a-695a-4b1f-94e7-f2ffa08440b7">CVssWriter::OnIdentify</a> or <a href="https://msdn.microsoft.com/4cb3b8f6-f702-4fba-a3cc-af84897cfd82">CVssWriterEx::OnIdentifyEx</a>.

To report component-level errors, writers should use the <a href="https://msdn.microsoft.com/f9fd728a-b205-4cfa-8e9e-e0a0d385f5a1">IVssComponentEx2::SetFailure</a> method.

If a writer's event handler (such as <a href="https://msdn.microsoft.com/2aff5e87-4053-46a0-a7fb-7411e76166ba">CVssWriter::OnFreeze</a>) calls this method, it must do so in the same thread that called the event handler. For more information, see 
<a href="writers.htm">Writer Event Handling</a>.




## -see-also




<a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>



<a href="https://msdn.microsoft.com/13cdeae3-dece-42ae-8bff-037ee3e4cec4">CVssWriterEx2</a>



<a href="https://msdn.microsoft.com/ab2be2c0-04bb-4a56-a636-ebd2c06e844a">IVssBackupComponentsEx3::GetWriterStatusEx</a>
 

 

