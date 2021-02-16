---
UID: NF:vswriter.CVssWriter.IsPathAffected
title: CVssWriter::IsPathAffected (vswriter.h)
description: The IsPathAffected method determines whether the specified directory or file is included in the current shadow copy set. The path for the directory or file can be a local path or a UNC path of a remote file share.
helpviewer_keywords: ["CVssWriter class [VSS]","IsPathAffected method","CVssWriter.IsPathAffected","CVssWriter::IsPathAffected","IsPathAffected","IsPathAffected method [VSS]","IsPathAffected method [VSS]","CVssWriter class","_win32_cvsswriter_ispathaffected","base.cvsswriter_ispathaffected","vswriter/CVssWriter::IsPathAffected"]
old-location: base\cvsswriter_ispathaffected.htm
tech.root: base
ms.assetid: 576e2e25-82dd-4b72-b777-0abc22a06386
ms.date: 12/05/2018
ms.keywords: CVssWriter class [VSS],IsPathAffected method, CVssWriter.IsPathAffected, CVssWriter::IsPathAffected, IsPathAffected, IsPathAffected method [VSS], IsPathAffected method [VSS],CVssWriter class, _win32_cvsswriter_ispathaffected, base.cvsswriter_ispathaffected, vswriter/CVssWriter::IsPathAffected
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
 - CVssWriter::IsPathAffected
 - vswriter/CVssWriter::IsPathAffected
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
 - CVssWriter.IsPathAffected
---

# CVssWriter::IsPathAffected


## -description

The <b>IsPathAffected</b> method determines whether 
    the specified directory or file is included in the current shadow copy set.  The path for the directory or file can be a local path or a UNC path of a remote file share.

<b>IsPathAffected</b> is a protected method 
    implemented by the <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class.

## -parameters

### -param wszPath [in]

Path of the directory or file to be queried. 
       This path can be a local path or a UNC path of a remote file share.

If the path refers to a directory, it can contain environment variables (for example, %SystemRoot%) but 
       cannot contain wildcard characters.

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
<dt><b>true</b></dt>
</dl>
</td>
<td width="60%">
The path is included in the set of volumes being included in the shadow copy set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>false</b></dt>
</dl>
</td>
<td width="60%">
The path is not included in the set of volumes being included in the shadow copy set.

</td>
</tr>
</table>

## -remarks

<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>Remote file shares are not supported until Windows 8 and Windows Server 2012. Writers support only local resources—sets of files whose absolute path starts with a 
    valid local volume specification and cannot be a mapped network drive. The input to 
    <b>IsPathAffected</b> (after the resolution of any 
    environment variables) must be in this format.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onfreeze">CVssWriter::OnFreeze</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparesnapshot">CVssWriter::OnPrepareSnapshot</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onthaw">CVssWriter::OnThaw</a>