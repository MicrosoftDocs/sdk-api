---
UID: NF:vswriter.IVssComponent.GetDifferencedFilesCount
title: IVssComponent::GetDifferencedFilesCount (vswriter.h)
description: Returns the number of file specifications in this component (and in any subcomponents of the component set it defines) marked by a writer supporting an incremental backup or restore as differenced files.
helpviewer_keywords: ["GetDifferencedFilesCount","GetDifferencedFilesCount method [VSS]","GetDifferencedFilesCount method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetDifferencedFilesCount method","IVssComponent.GetDifferencedFilesCount","IVssComponent::GetDifferencedFilesCount","_win32_ivsscomponent_getdifferencedfilescount","base.ivsscomponent_getdifferencedfilescount","vswriter/IVssComponent::GetDifferencedFilesCount"]
old-location: base\ivsscomponent_getdifferencedfilescount.htm
tech.root: base
ms.assetid: 46faeb2b-7d83-4618-ba36-bdacc5ca055d
ms.date: 12/05/2018
ms.keywords: GetDifferencedFilesCount, GetDifferencedFilesCount method [VSS], GetDifferencedFilesCount method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetDifferencedFilesCount method, IVssComponent.GetDifferencedFilesCount, IVssComponent::GetDifferencedFilesCount, _win32_ivsscomponent_getdifferencedfilescount, base.ivsscomponent_getdifferencedfilescount, vswriter/IVssComponent::GetDifferencedFilesCount
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IVssComponent::GetDifferencedFilesCount
 - vswriter/IVssComponent::GetDifferencedFilesCount
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
 - IVssComponent.GetDifferencedFilesCount
---

# IVssComponent::GetDifferencedFilesCount


## -description

The <b>GetDifferencedFilesCount</b> 
    method returns the number of file specifications in this component (and in any subcomponents of the 
    component set it defines) marked by a writer supporting an incremental backup or restore as differenced 
    files—that is, backup and restores associated with it are to be implemented as if 
    entire files are copied to and from backup media (as opposed to using partial files).

## -parameters

### -param pcDifferencedFiles [out]

The address of a caller-allocated variable that receives the number of differenced file specifications.

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
Successfully returned the attribute value.

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
</table>

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime">IVssComponent::AddDifferencedFilesByLastModifyTime</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getdifferencedfile">IVssComponent::GetDifferencedFile</a>



<a href="/windows/desktop/VSS/incremental-and-differential-backups">Incremental and Differential Backups</a>