---
UID: NF:vswriter.CVssWriter.AreComponentsSelected
title: CVssWriter::AreComponentsSelected (vswriter.h)
description: The AreComponentsSelected method indicates whether a requester is running under component mode and supports selecting individual components to be backed up or backs up entire volumes.
helpviewer_keywords: ["AreComponentsSelected","AreComponentsSelected method [VSS]","AreComponentsSelected method [VSS]","CVssWriter class","CVssWriter class [VSS]","AreComponentsSelected method","CVssWriter.AreComponentsSelected","CVssWriter::AreComponentsSelected","_win32_cvsswriter_arecomponentsselected","base.cvsswriter_arecomponentsselected","vswriter/CVssWriter::AreComponentsSelected"]
old-location: base\cvsswriter_arecomponentsselected.htm
tech.root: base
ms.assetid: da84f1ab-8712-436f-8ae7-ba3d52a761c0
ms.date: 12/05/2018
ms.keywords: AreComponentsSelected, AreComponentsSelected method [VSS], AreComponentsSelected method [VSS],CVssWriter class, CVssWriter class [VSS],AreComponentsSelected method, CVssWriter.AreComponentsSelected, CVssWriter::AreComponentsSelected, _win32_cvsswriter_arecomponentsselected, base.cvsswriter_arecomponentsselected, vswriter/CVssWriter::AreComponentsSelected
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
 - CVssWriter::AreComponentsSelected
 - vswriter/CVssWriter::AreComponentsSelected
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
 - CVssWriter.AreComponentsSelected
---

# CVssWriter::AreComponentsSelected


## -description

The 
<b>AreComponentsSelected</b> method indicates whether a requester is running under component mode and supports selecting individual components to be backed up or backs up entire volumes.

<b>AreComponentsSelected</b> is a protected method implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class.



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
The requester supports selecting components.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>false</b></dt>
</dl>
</td>
<td width="60%">
The requester does not support selecting components.

</td>
</tr>
</table>

## -remarks

If false is returned, it indicates that the backup application (requester) is not running under component mode.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onbackupcomplete">CVssWriter::OnBackupComplete</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore">CVssWriter::OnPostRestore</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CVssWriter::OnPreRestore</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a>
