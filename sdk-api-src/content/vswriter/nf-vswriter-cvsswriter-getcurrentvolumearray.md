---
UID: NF:vswriter.CVssWriter.GetCurrentVolumeArray
title: CVssWriter::GetCurrentVolumeArray
author: windows-sdk-content
description: The GetCurrentVolumeArray method returns the names of the original volumes and the UNC paths of the original remote file shares that belong to the shadow copy set as an array of null-terminated wide character strings.Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  Remote file shares are not supported until Windows 8 and Windows Server 2012.
old-location: base\cvsswriter_getcurrentvolumearray.htm
old-project: VSS
ms.assetid: 75f72b51-e940-4b1d-88a1-7c35de5a3d87
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: CVssWriter interface [VSS],GetCurrentVolumeArray method, CVssWriter.GetCurrentVolumeArray, CVssWriter::GetCurrentVolumeArray, GetCurrentVolumeArray, GetCurrentVolumeArray method [VSS], GetCurrentVolumeArray method [VSS],CVssWriter interface, _win32_cvsswriter_getcurrentvolumearray, base.cvsswriter_getcurrentvolumearray, vswriter/CVssWriter::GetCurrentVolumeArray
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	CVssWriter.GetCurrentVolumeArray
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# CVssWriter::GetCurrentVolumeArray


## -description


The 
<b>GetCurrentVolumeArray</b> method returns the names of the original volumes and the UNC paths of the original remote file shares that belong to the shadow copy set as an array of null-terminated wide character strings.<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>Remote file shares are not supported until Windows 8 and Windows Server 2012.



<b>GetCurrentVolumeArray</b> is a protected method implemented by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class.


## -parameters






## -returns



This method returns a pointer to an <i>n</i>-element array (where <i>n</i> is the value returned by 
<a href="https://msdn.microsoft.com/5f553a46-10ee-475e-b028-2652c74fbe5d">CVssWriter::GetCurrentVolumeCount</a>) of null-terminated wide character strings that contain the names of the original volumes and the UNC paths of the original remote file shares that belong to the shadow copy set.<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>Remote file shares are not supported until Windows 8 and Windows Server 2012.



The derived class should not free the memory held by the returned array of volume names. The base class manages the life cycle of the array.




## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/2aff5e87-4053-46a0-a7fb-7411e76166ba">CVssWriter::OnFreeze</a>



<a href="https://msdn.microsoft.com/a077323e-d04c-4bf7-8aa6-5028fa1c6e6b">CVssWriter::OnPrepareSnapshot</a>



<a href="https://msdn.microsoft.com/36028e9f-f7a7-41f1-a570-48f943e9ab83">CVssWriter::OnThaw</a>
 

 

