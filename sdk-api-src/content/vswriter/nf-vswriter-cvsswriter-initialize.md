---
UID: NF:vswriter.CVssWriter.Initialize
title: CVssWriter::Initialize (vswriter.h)
description: Initializes a CVssWriter object and allows a writer application to interact with VSS.
helpviewer_keywords: ["CVssWriter interface [VSS]","Initialize method","CVssWriter.Initialize","CVssWriter::Initialize","Initialize","Initialize method [VSS]","Initialize method [VSS]","CVssWriter interface","_win32_cvsswriter_initialize","base.cvsswriter_initialize","vswriter/CVssWriter::Initialize"]
old-location: base\cvsswriter_initialize.htm
tech.root: base
ms.assetid: a427ebbd-b7c4-46ba-ba16-dd601b1f956e
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],Initialize method, CVssWriter.Initialize, CVssWriter::Initialize, Initialize, Initialize method [VSS], Initialize method [VSS],CVssWriter interface, _win32_cvsswriter_initialize, base.cvsswriter_initialize, vswriter/CVssWriter::Initialize
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
 - CVssWriter::Initialize
 - vswriter/CVssWriter::Initialize
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
 - CVssWriter.Initialize
---

# CVssWriter::Initialize


## -description

Initializes a 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> object and allows a writer application to interact with VSS.

<b>Initialize</b> is a public method implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class.

## -parameters

### -param WriterId [in]

The globally unique identifier (GUID) of the writer class.

### -param wszWriterName [in]

A <b>null</b>-terminated wide character string that contains the name of the writer. This string is not localized.

### -param ut [in]

A <a href="/windows/desktop/api/vswriter/ne-vswriter-vss_usage_type">VSS_USAGE_TYPE</a> enumeration value that indicates how the data managed by the writer is used on the host system.

### -param st [in]

A
      <a href="/windows/desktop/api/vswriter/ne-vswriter-vss_source_type">VSS_SOURCE_TYPE</a> enumeration value that indicates the type of data managed by the writer.

### -param nLevel [in]

A
      <a href="/windows/desktop/api/vss/ne-vss-vss_application_level">VSS_APPLICATION_LEVEL</a> enumeration value that indicates the application level at which the writer receives a <a href="/windows/desktop/VSS/vssgloss-f">Freeze</a> event notification. 




The default value for this parameter is VSS_APP_FRONT_END.

### -param dwTimeoutFreeze [in]

The maximum permitted time, in milliseconds, between a writer's receipt of a <a href="/windows/desktop/VSS/vssgloss-f">Freeze</a> event notification and the receipt of a matching <a href="/windows/desktop/VSS/vssgloss-t">Thaw</a> event notification from VSS. After the time-out expires, the writer's 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onabort">CVssWriter::OnAbort</a> method is called automatically. 




The default value for this parameter is 60000.

### -param aws [in]

A <a href="/windows/desktop/api/vswriter/ne-vswriter-vss_alternate_writer_state">VSS_ALTERNATE_WRITER_STATE</a> enumeration value that indicates whether the writer has an associated alternate writer. 




The default value for this parameter is VSS_AWS_NO_ALTERNATE_WRITER. The caller should not override this default value. This parameter is reserved for future use.

### -param bIOThrottlingOnly [in]

Set this parameter to <b>true</b>  if I/O throttling methods are enabled, or <b>false</b> otherwise. 




The default value for this parameter is <b>false</b>. The caller should not override this default value. This parameter is reserved for future use.

### -param wszWriterInstanceName [in]

A <b>null</b>-terminated wide character string that contains the writer instance name. 




The default value for this parameter is <b>NULL</b>. If the writer has multiple instances and requires restore events, this parameter is required and cannot be <b>NULL</b>. For details, see the following Remarks section.

<b>Windows Server 2003 and Windows XP:  </b>Before Windows Server 2003 with SP1, this parameter is reserved for system use, and the caller should not override the default value.

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
Successfully initialized the writer object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The writer object could not be initialized; the VSS writer infrastructure was inactive because Windows was in safe mode or was setting up.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller is not an administrator.

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

VSS assigns a unique writer instance ID to each instance of a writer application. If more than one instance is present on the system at the same time (for example, if multiple SQL servers are running on a system), each writer is uniquely identified by the combination of its writer class ID and its writer instance ID.

The <i>wszWriterInstanceName</i> parameter allows a multi-instance writer to specify a persistent name for each writer instance as a human-readable string. This name must be unique across all instances of the writer on the system. If a writer has multiple instances and requires restore events, it must specify a non-<b>NULL</b> string for this parameter. VSS uses the instance name to correctly restore multi-instance writers.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onabort">CVssWriter::OnAbort</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_alternate_writer_state">VSS_ALTERNATE_WRITER_STATE</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_application_level">VSS_APPLICATION_LEVEL</a>



<a href="/windows/desktop/VSS/volume-shadow-copy-api-data-types">VSS_ID</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_source_type">VSS_SOURCE_TYPE</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_usage_type">VSS_USAGE_TYPE</a>