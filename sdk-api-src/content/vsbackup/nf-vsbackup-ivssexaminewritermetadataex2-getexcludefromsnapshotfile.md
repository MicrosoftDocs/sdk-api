---
UID: NF:vsbackup.IVssExamineWriterMetadataEx2.GetExcludeFromSnapshotFile
title: IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotFile (vsbackup.h)
description: Obtains information about file sets that have been explicitly excluded from a given shadow copy.
helpviewer_keywords: ["GetExcludeFromSnapshotFile","GetExcludeFromSnapshotFile method","GetExcludeFromSnapshotFile method","IVssExamineWriterMetadataEx2 interface","IVssExamineWriterMetadataEx2 interface","GetExcludeFromSnapshotFile method","IVssExamineWriterMetadataEx2.GetExcludeFromSnapshotFile","IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotFile","base.ivssexaminewritermetadataex2_getexcludefromsnapshotfile","vsbackup/IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotFile"]
old-location: base\ivssexaminewritermetadataex2_getexcludefromsnapshotfile.htm
tech.root: base
ms.assetid: 3df57749-9a26-4187-b1fc-aeb68a4d1d06
ms.date: 12/05/2018
ms.keywords: GetExcludeFromSnapshotFile, GetExcludeFromSnapshotFile method, GetExcludeFromSnapshotFile method,IVssExamineWriterMetadataEx2 interface, IVssExamineWriterMetadataEx2 interface,GetExcludeFromSnapshotFile method, IVssExamineWriterMetadataEx2.GetExcludeFromSnapshotFile, IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotFile, base.ivssexaminewritermetadataex2_getexcludefromsnapshotfile, vsbackup/IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotFile
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotFile
 - vsbackup/IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotFile
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
 - IVssExamineWriterMetadataEx2.GetExcludeFromSnapshotFile
---

# IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotFile


## -description

Obtains information about <a href="/windows/desktop/VSS/vssgloss-f">file sets</a> that have been explicitly excluded from a given shadow copy.

## -parameters

### -param iFile [in]

An index for an excluded <a href="/windows/desktop/VSS/vssgloss-f">file set</a>. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of <i>file sets</i> explicitly excluded from a given shadow copy. The value of <i>n</i> is returned by 
the <b>IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotCount</b> method.

### -param ppFiledesc [out]

A doubly indirect pointer to an 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object containing the file element information.

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
The pointer to an 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> interface was successfully returned.

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

The caller is responsible for calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method to release the resources of the returned 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object.

The <b>GetExcludeFromSnapshotFile</b> method is intended to report information about <a href="/windows/desktop/VSS/vssgloss-f">file sets</a> excluded from a shadow copy. Requesters should not exclude files from backup based on the information returned by this method.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot">IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadataex2">IVssExamineWriterMetadataEx2</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadataex2-getexcludefromsnapshotfile">IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotCount</a>