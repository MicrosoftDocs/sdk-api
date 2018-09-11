---
UID: NF:vswriter.CVssWriter.GetBackupType
title: CVssWriter::GetBackupType
author: windows-sdk-content
description: The GetBackupType method indicates the type of backup to be performed.
old-location: base\cvsswriter_getbackuptype.htm
tech.root: VSS
ms.assetid: b8f78552-27b5-4d64-9d35-baf1c636b526
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CVssWriter interface [VSS],GetBackupType method, CVssWriter.GetBackupType, CVssWriter::GetBackupType, GetBackupType, GetBackupType method [VSS], GetBackupType method [VSS],CVssWriter interface, _win32_cvsswriter_getbackuptype, base.cvsswriter_getbackuptype, vswriter/CVssWriter::GetBackupType
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
 - CVssWriter.GetBackupType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CVssWriter::GetBackupType


## -description


The 
<b>GetBackupType</b> method indicates the type of backup to be performed.

<b>GetBackupType</b> is a protected method implemented by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class.


## -parameters






## -returns



This method returns the backup type as a 
<a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a> enumeration value. See 
<b>VSS_BACKUP_TYPE</b> for a description of these values.




## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/77d0621d-81bd-4d53-8e5d-f5d3bfd86013">CVssWriter::OnBackupComplete</a>



<a href="https://msdn.microsoft.com/ad07753c-1592-4fc8-9899-a73e798c158c">CVssWriter::OnPostRestore</a>



<a href="https://msdn.microsoft.com/5f4a6168-4102-4790-81d6-d195a440471f">CVssWriter::OnPreRestore</a>



<a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">CVssWriter::OnPrepareBackup</a>



<a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a>
 

 

