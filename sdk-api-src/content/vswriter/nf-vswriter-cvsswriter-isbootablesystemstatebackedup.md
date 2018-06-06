---
UID: NF:vswriter.CVssWriter.IsBootableSystemStateBackedUp
title: CVssWriter::IsBootableSystemStateBackedUp
author: windows-sdk-content
description: The IsBootableSystemStateBackedUp method indicates whether the bootable state will be backed up.
old-location: base\cvsswriter_isbootablestatebackedup.htm
old-project: VSS
ms.assetid: 2ab7628e-c5d4-4a08-bc34-47356aee94bf
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: CVssWriter class [VSS],IsBootableSystemStateBackedUp method, CVssWriter.IsBootableSystemStateBackedUp, CVssWriter::IsBootableSystemStateBackedUp, IsBootableSystemStateBackedUp, IsBootableSystemStateBackedUp method [VSS], IsBootableSystemStateBackedUp method [VSS],CVssWriter class, _win32_cvsswriter_isbootablestatebackedup, base.cvsswriter_isbootablestatebackedup, vswriter/CVssWriter::IsBootableSystemStateBackedUp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VSS_WRITERRESTORE_ENUM
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
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# CVssWriter::IsBootableSystemStateBackedUp


## -description


The 
<b>IsBootableSystemStateBackedUp</b> method indicates whether the bootable state will be backed up.

<b>IsBootableSystemStateBackedUp</b> is a protected method implemented by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class.


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




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/77d0621d-81bd-4d53-8e5d-f5d3bfd86013">CVssWriter::OnBackupComplete</a>



<a href="https://msdn.microsoft.com/ad07753c-1592-4fc8-9899-a73e798c158c">CVssWriter::OnPostRestore</a>



<a href="https://msdn.microsoft.com/5f4a6168-4102-4790-81d6-d195a440471f">CVssWriter::OnPreRestore</a>



<a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">CVssWriter::OnPrepareBackup</a>
 

 

