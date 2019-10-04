---
UID: NF:vswriter.CVssWriter.IsBootableSystemStateBackedUp
title: CVssWriter::IsBootableSystemStateBackedUp (vswriter.h)
author: windows-sdk-content
description: The IsBootableSystemStateBackedUp method indicates whether the bootable state will be backed up.
old-location: base\cvsswriter_isbootablestatebackedup.htm
tech.root: VSS
ms.assetid: 2ab7628e-c5d4-4a08-bc34-47356aee94bf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CVssWriter class [VSS],IsBootableSystemStateBackedUp method, CVssWriter.IsBootableSystemStateBackedUp, CVssWriter::IsBootableSystemStateBackedUp, IsBootableSystemStateBackedUp, IsBootableSystemStateBackedUp method [VSS], IsBootableSystemStateBackedUp method [VSS],CVssWriter class, _win32_cvsswriter_isbootablestatebackedup, base.cvsswriter_isbootablestatebackedup, vswriter/CVssWriter::IsBootableSystemStateBackedUp
ms.topic: method
f1_keywords: 
 - "vswriter/CVssWriter.IsBootableSystemStateBackedUp"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - CVssWriter.IsBootableSystemStateBackedUp
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CVssWriter::IsBootableSystemStateBackedUp


## -description


The 
<b>IsBootableSystemStateBackedUp</b> method indicates whether the bootable state will be backed up.

<b>IsBootableSystemStateBackedUp</b> is a protected method implemented by the 
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class.


## -parameters






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
Bootable system state will be backed up.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>false</b></dt>
</dl>
</td>
<td width="60%">
Bootable system state will not be backed up.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onbackupcomplete">CVssWriter::OnBackupComplete</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore">CVssWriter::OnPostRestore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CVssWriter::OnPreRestore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a>
 

 

