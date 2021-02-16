---
UID: NF:vswriter.IVssWMFiledesc.GetRecursive
title: IVssWMFiledesc::GetRecursive (vswriter.h)
description: Indicates whether the list of files described in a IVssWMFiledesc object with a root directory returned by IVssWMFiledesc::GetPath contains only files in that directory.
helpviewer_keywords: ["GetRecursive","GetRecursive method [VSS]","GetRecursive method [VSS]","IVssWMFiledesc interface","IVssWMFiledesc interface [VSS]","GetRecursive method","IVssWMFiledesc.GetRecursive","IVssWMFiledesc::GetRecursive","_win32_ivsswmfiledesc_getrecursive","base.ivsswmfiledesc_getrecursive","vswriter/IVssWMFiledesc::GetRecursive"]
old-location: base\ivsswmfiledesc_getrecursive.htm
tech.root: base
ms.assetid: f467bd6f-997b-4d5f-87a4-727d9a84a222
ms.date: 12/05/2018
ms.keywords: GetRecursive, GetRecursive method [VSS], GetRecursive method [VSS],IVssWMFiledesc interface, IVssWMFiledesc interface [VSS],GetRecursive method, IVssWMFiledesc.GetRecursive, IVssWMFiledesc::GetRecursive, _win32_ivsswmfiledesc_getrecursive, base.ivsswmfiledesc_getrecursive, vswriter/IVssWMFiledesc::GetRecursive
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
 - IVssWMFiledesc::GetRecursive
 - vswriter/IVssWMFiledesc::GetRecursive
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
 - IVssWMFiledesc.GetRecursive
---

# IVssWMFiledesc::GetRecursive


## -description

The <b>GetRecursive</b> method 
    indicates whether the list of files described in a 
    <a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object with a root directory returned by 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsswmfiledesc-getpath">IVssWMFiledesc::GetPath</a> contains only files in 
    that directory or whether the file list contains files from the directory hierarchy as well.

## -parameters

### -param pbRecursive [out]

A pointer to a Boolean value specifying whether the value returned by 
      <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsswmfiledesc-getpath">IVssWMFiledesc::GetPath</a> identifies 
      only a single directory or if it indicates a hierarchy of directories to be traversed recursively. The Boolean value receives 
      <b>true</b> if the path is treated as a hierarchy of directories to be traversed recursively, or <b>false</b> if not.
      

For information on traversing over mounted folders, see 
       <a href="/windows/desktop/VSS/working-with-reparse-and-mount-points">Working with Mounted Folders and Reparse Points</a>.

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
Successfully returned the recursive information.

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
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more 
        information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a>