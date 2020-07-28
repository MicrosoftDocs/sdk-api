---
UID: NF:vswriter.CVssWriterEx.InitializeEx
title: CVssWriterEx::InitializeEx (vswriter.h)
description: Initializes a CVssWriterEx object and allows a writer application to interact with VSS. Unlike the Initialize method, the InitializeEx method allows the caller to specify writer version information.
helpviewer_keywords: ["CVssWriterEx interface","InitializeEx method","CVssWriterEx.InitializeEx","CVssWriterEx::InitializeEx","InitializeEx","InitializeEx method","InitializeEx method","CVssWriterEx interface","base.cvsswriterex_initializeex","vswriter/CVssWriterEx::InitializeEx"]
old-location: base\cvsswriterex_initializeex.htm
tech.root: base
ms.assetid: 08516a5e-b1ad-4256-9eee-261393b031e2
ms.date: 12/05/2018
ms.keywords: CVssWriterEx interface,InitializeEx method, CVssWriterEx.InitializeEx, CVssWriterEx::InitializeEx, InitializeEx, InitializeEx method, InitializeEx method,CVssWriterEx interface, base.cvsswriterex_initializeex, vswriter/CVssWriterEx::InitializeEx
f1_keywords:
- vswriter/CVssWriterEx.InitializeEx
dev_langs:
- c++
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- VssApi.lib
- VssApi.dll
api_name:
- CVssWriterEx.InitializeEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CVssWriterEx::InitializeEx


## -description


Initializes a 
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-cvsswriterex">CVssWriterEx</a> object and allows a writer application to interact with VSS. Unlike the <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">Initialize</a> method, the <b>InitializeEx</b> method allows the caller to specify writer version information.

<b>InitializeEx</b> is a public method implemented by the 
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-cvsswriterex">CVssWriterEx</a> base class.

Writers must call <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">Initialize</a> or <b>InitializeEx</b>, but not both.


## -parameters




### -param WriterId [in]

The globally unique identifier (GUID) of the writer class.


### -param wszWriterName [in]

A <b>null</b>-terminated wide character string that contains the name of the writer. This string is not localized.


### -param dwMajorVersion [in]

The major version of the writer application. For more information, see the Remarks section.


### -param dwMinorVersion [in]

The minor version of the writer application. For more information, see the Remarks section.


### -param ut [in]

A <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/ne-vswriter-vss_usage_type">VSS_USAGE_TYPE</a> enumeration value that indicates how the data that is managed by the writer is used on the host system.


### -param st [in]

A 
      <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/ne-vswriter-vss_source_type">VSS_SOURCE_TYPE</a> enumeration value that indicates the type of data that is managed by the writer.


### -param nLevel [in]

A 
      <a href="https://docs.microsoft.com/windows/desktop/api/vss/ne-vss-vss_application_level">VSS_APPLICATION_LEVEL</a> enumeration value that indicates the application level at which the writer receives a <a href="https://docs.microsoft.com/windows/desktop/VSS/vssgloss-f">Freeze</a> event notification. 




The default value for this parameter is VSS_APP_FRONT_END.


### -param dwTimeoutFreeze [in]

The maximum permitted time, in milliseconds, between the writer's  receipt of a <a href="https://docs.microsoft.com/windows/desktop/VSS/vssgloss-f">Freeze</a> event notification and its receipt of a matching <a href="https://docs.microsoft.com/windows/desktop/VSS/vssgloss-t">Thaw</a> event notification from VSS. After the time-out expires, the writer's 
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onabort">OnAbort</a> method is called automatically. 




The default value for this parameter is 60000.


### -param aws [in]

A <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/ne-vswriter-vss_alternate_writer_state">VSS_ALTERNATE_WRITER_STATE</a> enumeration value that indicates whether the writer has an associated alternate writer. 




The default value for this parameter is VSS_AWS_NO_ALTERNATE_WRITER. The caller should not override this default value. This parameter is reserved for future use.


### -param bIOThrottlingOnly [in]

Set this parameter to <b>true</b>  if I/O throttling methods are enabled, or <b>false</b> otherwise. 




The default value for this parameter is <b>false</b>. The caller should not override this default value. This parameter is reserved for future use.


### -param wszWriterInstanceName [in]

A <b>null</b>-terminated wide character string that contains the writer instance name. 




The default value for this parameter is <b>NULL</b>. If the writer has multiple instances and requires restore events, this parameter is required and cannot be <b>NULL</b>. For more information, see the following Remarks section.


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
The writer object was successfully initialized.

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
        <a href="https://docs.microsoft.com/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>
 




## -remarks



The <b>InitializeEx</b> method is identical to the <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">Initialize</a> method except for the <i>dwMajorVersion</i> and <i>dwMinorVersion</i> parameters. If the writer uses <b>Initialize</b> instead of <b>InitializeEx</b>, the writer version will be reported as 0.0 (major version = 0, minor version = 0) by the <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadataex2-getversion">IVssExamineWriterMetadataEx2::GetVersion</a> method.

The <i>dwMajorVersion</i> and <i>dwMinorVersion</i> parameters are used to specify the writer major and minor version numbers according to the following VSS conventions:

<ul>
<li>If the writer has changed since Windows XP or is new for Windows Vista, it should specify 1.0 or higher for its version number.</li>
<li>A writer's minor version number should be incremented by one whenever a released version of the writer contains minor changes that affect the writer's interaction with requesters. For example, a correction to a file specification in a writer QFE or service pack would justify incrementing the minor version number. However, a change between beta or release candidate versions of a writer would not justify the changing of the minor version number.</li>
<li>A writer's major version number should be incremented by one whenever a released version of the writer contains a significant change. For example, if data that is backed up with a new version of a writer cannot be restored using the previous version of the writer, the new writer's major version number should be incremented.</li>
<li>Whenever the major version number is incremented, the minor version number should be reset to zero.</li>
</ul>
If a writer does not specify a version number, VSS will assign a default version number of 0.0.

VSS assigns a unique writer instance ID to each instance of a writer application. If more than one instance is present on the system at the same time (for example, if multiple SQL servers are running on a system), each writer is uniquely identified by the combination of its writer class ID and its writer instance ID.

The <i>wszWriterInstanceName</i> parameter allows a multi-instance writer to specify a persistent name for each writer instance as a human-readable string. This name must be unique across all instances of the writer on the system. If a writer has multiple instances and requires restore events, it must specify a non-<b>NULL</b> string for this parameter. VSS uses the instance name to correctly restore multi-instance writers.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-cvsswriterex">CVssWriterEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadataex2-getversion">IVssExamineWriterMetadataEx2::GetVersion</a>
 

 

