---
UID: NF:vswriter.CVssWriter.GetCurrentLevel
title: CVssWriter::GetCurrentLevel method
author: windows-driver-content
description: The GetCurrentLevel method returns the current application level.
old-location: base\cvsswriter_getcurrentlevel.htm
old-project: VSS
ms.assetid: 09540f57-832a-49ca-9b64-e7660b331192
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: CVssWriter, CVssWriter interface [VSS], GetCurrentLevel method, CVssWriter::GetCurrentLevel, GetCurrentLevel method [VSS], GetCurrentLevel method [VSS], CVssWriter interface, GetCurrentLevel,CVssWriter.GetCurrentLevel, _win32_cvsswriter_getcurrentlevel, base.cvsswriter_getcurrentlevel, vswriter/CVssWriter::GetCurrentLevel
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
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	CVssWriter.GetCurrentLevel
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# CVssWriter::GetCurrentLevel method


## -description


The 
<b>GetCurrentLevel</b> method returns the current application level.

<b>GetCurrentLevel</b> is a protected method implemented by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class.


## -parameters






## -returns



This method returns a writer's current application level as a 
<a href="https://msdn.microsoft.com/fc7fbaee-d223-4557-987d-2c09f3877ec2">VSS_APPLICATION_LEVEL</a> enumeration value. See 
<b>VSS_APPLICATION_LEVEL</b> for a description of these values.




## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/2aff5e87-4053-46a0-a7fb-7411e76166ba">CVssWriter::OnFreeze</a>



<a href="https://msdn.microsoft.com/a077323e-d04c-4bf7-8aa6-5028fa1c6e6b">CVssWriter::OnPrepareSnapshot</a>



<a href="https://msdn.microsoft.com/36028e9f-f7a7-41f1-a570-48f943e9ab83">CVssWriter::OnThaw</a>



<a href="https://msdn.microsoft.com/fc7fbaee-d223-4557-987d-2c09f3877ec2">VSS_APPLICATION_LEVEL</a>
 

 

