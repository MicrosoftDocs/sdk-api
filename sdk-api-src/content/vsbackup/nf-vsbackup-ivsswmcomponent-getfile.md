---
UID: NF:vsbackup.IVssWMComponent.GetFile
title: IVssWMComponent::GetFile (vsbackup.h)
description: The GetFile method obtains a file descriptor associated with a file group.
helpviewer_keywords: ["GetFile","GetFile method [VSS]","GetFile method [VSS]","IVssWMComponent interface","IVssWMComponent interface [VSS]","GetFile method","IVssWMComponent.GetFile","IVssWMComponent::GetFile","_win32_ivsswmcomponent_getfile","base.ivsswmcomponent_getfile","vsbackup/IVssWMComponent::GetFile"]
old-location: base\ivsswmcomponent_getfile.htm
tech.root: base
ms.assetid: 55956a05-59b8-4197-8496-03903b6e0faa
ms.date: 12/05/2018
ms.keywords: GetFile, GetFile method [VSS], GetFile method [VSS],IVssWMComponent interface, IVssWMComponent interface [VSS],GetFile method, IVssWMComponent.GetFile, IVssWMComponent::GetFile, _win32_ivsswmcomponent_getfile, base.ivsswmcomponent_getfile, vsbackup/IVssWMComponent::GetFile
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
 - IVssWMComponent::GetFile
 - vsbackup/IVssWMComponent::GetFile
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
 - IVssWMComponent.GetFile
---

# IVssWMComponent::GetFile


## -description

The 
<b>GetFile</b> method obtains a file descriptor associated with a file group.

## -parameters

### -param iFile [in]

Offset between 0 and <i>n</i>-1, where <i>n</i> is the number of files in the file group as specified by the <b>cFileCount</b> member of the 
<a href="/windows/desktop/api/vsbackup/ns-vsbackup-vss_componentinfo">VSS_COMPONENTINFO</a> object returned by 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getcomponentinfo">IVssWMComponent::GetComponentInfo</a>.

### -param ppFiledesc [out]

Doubly indirect pointer to a 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object containing the returned file descriptor information.

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
Successfully returned a pointer to an instance of the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> interface.

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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified file does not exist.

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

The caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release system resources held by the returned 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswmcomponent">IVssWMComponent</a>