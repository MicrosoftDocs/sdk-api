---
UID: NF:vswriter.IVssWMFiledesc.GetFilespec
title: IVssWMFiledesc::GetFilespec (vswriter.h)
description: The GetFilespec method returns the file specification used to obtain the list of files that the current IVssWMFiledesc object is a member of.
helpviewer_keywords: ["GetFilespec","GetFilespec method [VSS]","GetFilespec method [VSS]","IVssWMFiledesc interface","IVssWMFiledesc interface [VSS]","GetFilespec method","IVssWMFiledesc.GetFilespec","IVssWMFiledesc::GetFilespec","_win32_ivsswmfiledesc_getfilespec","base.ivsswmfiledesc_getfilespec","vswriter/IVssWMFiledesc::GetFilespec"]
old-location: base\ivsswmfiledesc_getfilespec.htm
tech.root: base
ms.assetid: 9661d22b-5c82-412d-966d-83605c568e22
ms.date: 12/05/2018
ms.keywords: GetFilespec, GetFilespec method [VSS], GetFilespec method [VSS],IVssWMFiledesc interface, IVssWMFiledesc interface [VSS],GetFilespec method, IVssWMFiledesc.GetFilespec, IVssWMFiledesc::GetFilespec, _win32_ivsswmfiledesc_getfilespec, base.ivsswmfiledesc_getfilespec, vswriter/IVssWMFiledesc::GetFilespec
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
 - IVssWMFiledesc::GetFilespec
 - vswriter/IVssWMFiledesc::GetFilespec
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
 - IVssWMFiledesc.GetFilespec
---

# IVssWMFiledesc::GetFilespec


## -description

The 
<b>GetFilespec</b> method returns the file specification used to obtain the list of files that the current 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object is a member of.

A querying method used a path and this file specification to return the current 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object.

## -parameters

### -param pbstrFilespec [out]

The address of a caller-allocated variable that receives a string specifying the returned file specification. 




A file specification cannot contain directory specifications (for example, no backslashes) but can contain the ? and * wildcard characters.

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
Successfully returned the filespec information.

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

The caller must call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory held by the <i>pbstrFilespec</i> parameter.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a>