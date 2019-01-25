---
UID: NF:vswriter.CVssWriter.GetCurrentVolumeCount
title: CVssWriter::GetCurrentVolumeCount
author: windows-sdk-content
description: The GetCurrentVolumeCount method returns the number of volumes in the shadow copy set.
old-location: base\cvsswriter_getcurrentvolumecount.htm
tech.root: VSS
ms.assetid: 5f553a46-10ee-475e-b028-2652c74fbe5d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CVssWriter interface [VSS],GetCurrentVolumeCount method, CVssWriter.GetCurrentVolumeCount, CVssWriter::GetCurrentVolumeCount, GetCurrentVolumeCount, GetCurrentVolumeCount method [VSS], GetCurrentVolumeCount method [VSS],CVssWriter interface, _win32_cvsswriter_getcurrentvolumecount, base.cvsswriter_getcurrentvolumecount, vswriter/CVssWriter::GetCurrentVolumeCount
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
 - CVssWriter.GetCurrentVolumeCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CVssWriter::GetCurrentVolumeCount


## -description


The 
<b>GetCurrentVolumeCount</b> method returns the number of volumes in the shadow copy set.

<b>GetCurrentVolumeCount</b> is a protected method implemented by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class.


## -parameters






## -returns



This method returns the number of volumes returned in the shadow copy set. This value will also be the size of the array of null-terminated wide character strings containing volume names returned by 
<a href="https://msdn.microsoft.com/75f72b51-e940-4b1d-88a1-7c35de5a3d87">CVssWriter::GetCurrentVolumeArray</a>.




## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/75f72b51-e940-4b1d-88a1-7c35de5a3d87">CVssWriter::GetCurrentVolumeArray</a>



<a href="https://msdn.microsoft.com/2aff5e87-4053-46a0-a7fb-7411e76166ba">CVssWriter::OnFreeze</a>



<a href="https://msdn.microsoft.com/a077323e-d04c-4bf7-8aa6-5028fa1c6e6b">CVssWriter::OnPrepareSnapshot</a>



<a href="https://msdn.microsoft.com/36028e9f-f7a7-41f1-a570-48f943e9ab83">CVssWriter::OnThaw</a>
 

 

