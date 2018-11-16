---
UID: NF:vswriter.CVssWriter.AreComponentsSelected
title: CVssWriter::AreComponentsSelected
author: windows-sdk-content
description: The AreComponentsSelected method indicates whether a requester is running under component mode and supports selecting individual components to be backed up or backs up entire volumes.
old-location: base\cvsswriter_arecomponentsselected.htm
tech.root: VSS
ms.assetid: da84f1ab-8712-436f-8ae7-ba3d52a761c0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AreComponentsSelected, AreComponentsSelected method [VSS], AreComponentsSelected method [VSS],CVssWriter class, CVssWriter class [VSS],AreComponentsSelected method, CVssWriter.AreComponentsSelected, CVssWriter::AreComponentsSelected, _win32_cvsswriter_arecomponentsselected, base.cvsswriter_arecomponentsselected, vswriter/CVssWriter::AreComponentsSelected
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - CVssWriter.AreComponentsSelected
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vswriter.h
: 
- CVssWriter.AreComponentsSelected
: 
---

# CVssWriter::AreComponentsSelected


## -description


The 
<b>AreComponentsSelected</b> method indicates whether a requester is running under component mode and supports selecting individual components to be backed up or backs up entire volumes.

<b>AreComponentsSelected</b> is a protected method implemented by the 
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




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/77d0621d-81bd-4d53-8e5d-f5d3bfd86013">CVssWriter::OnBackupComplete</a>



<a href="https://msdn.microsoft.com/ad07753c-1592-4fc8-9899-a73e798c158c">CVssWriter::OnPostRestore</a>



<a href="https://msdn.microsoft.com/5f4a6168-4102-4790-81d6-d195a440471f">CVssWriter::OnPreRestore</a>



<a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">CVssWriter::OnPrepareBackup</a>
 

 

