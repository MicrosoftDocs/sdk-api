---
UID: NF:vswriter.IVssWMFiledesc.GetAlternateLocation
title: IVssWMFiledesc::GetAlternateLocation (vswriter.h)
description: The GetAlternateLocation method obtains an alternate location for a file set.
helpviewer_keywords: ["GetAlternateLocation","GetAlternateLocation method [VSS]","GetAlternateLocation method [VSS]","IVssWMFiledesc interface","IVssWMFiledesc interface [VSS]","GetAlternateLocation method","IVssWMFiledesc.GetAlternateLocation","IVssWMFiledesc::GetAlternateLocation","_win32_ivsswmfiledesc_getalternatelocation","base.ivsswmfiledesc_getalternatelocation","vswriter/IVssWMFiledesc::GetAlternateLocation"]
old-location: base\ivsswmfiledesc_getalternatelocation.htm
tech.root: base
ms.assetid: 3bb787eb-ac15-40d0-9901-b869442399c5
ms.date: 12/05/2018
ms.keywords: GetAlternateLocation, GetAlternateLocation method [VSS], GetAlternateLocation method [VSS],IVssWMFiledesc interface, IVssWMFiledesc interface [VSS],GetAlternateLocation method, IVssWMFiledesc.GetAlternateLocation, IVssWMFiledesc::GetAlternateLocation, _win32_ivsswmfiledesc_getalternatelocation, base.ivsswmfiledesc_getalternatelocation, vswriter/IVssWMFiledesc::GetAlternateLocation
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
 - IVssWMFiledesc::GetAlternateLocation
 - vswriter/IVssWMFiledesc::GetAlternateLocation
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
 - IVssWMFiledesc.GetAlternateLocation
---

# IVssWMFiledesc::GetAlternateLocation


## -description

The 
<b>GetAlternateLocation</b> method obtains an alternate location for a file set.

## -parameters

### -param pbstrAlternateLocation [out]

The address of a caller-allocated variable that receives a string specifying the alternate backup location. The path of this location can be a local path or the UNC path of a remote file share. If there is no alternate location, the pointer is <b>NULL</b>.

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
Successfully returned the alternate location information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The requested information could not be found.

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

<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>Remote file shares are not supported until Windows 8 and Windows Server 2012.

The caller must call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory held by the <i>pbstrAlternateLocation</i> parameter.

The interpretation of the alternate location returned by 
<b>GetAlternateLocation</b> differs depending on the method used to retrieve the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object.



<ul>
<li>
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile">IVssExamineWriterMetadata::GetExcludeFile</a>
</li>
<li>
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getdatabasefile">IVssWMComponent::GetDatabaseFile</a>
</li>
<li>
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile">IVssWMComponent::GetDatabaseLogFile</a>
</li>
<li>
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getfile">IVssWMComponent::GetFile</a>
</li>
</ul>
The value returned by 
<b>GetAlternateLocation</b> refers to an alternate location mapping when returned by the 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping">IVssExamineWriterMetadata::GetAlternateLocationMapping</a> method.

During backup operations, this is the alternate location from which to back up a file. During a restore, it is the alternate location to which to restore a file.

For more information, see 
<a href="/windows/desktop/VSS/non-default-backup-and-restore-locations">Non-Default Backup And Restore Locations</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a>