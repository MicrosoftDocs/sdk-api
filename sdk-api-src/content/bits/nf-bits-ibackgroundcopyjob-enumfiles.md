---
UID: NF:bits.IBackgroundCopyJob.EnumFiles
title: IBackgroundCopyJob::EnumFiles
author: windows-sdk-content
description: Retrieves an IEnumBackgroundCopyFiles interface pointer that you use to enumerate the files in a job.
old-location: bits\ibackgroundcopyjob_enumfiles.htm
tech.root: bits
ms.assetid: c6b8ef69-9c67-447f-9f90-b6905a5a5a19
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: EnumFiles, EnumFiles method [BITS], EnumFiles method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],EnumFiles method, IBackgroundCopyJob.EnumFiles, IBackgroundCopyJob::EnumFiles, _drz_ibackgroundcopyjob_enumfiles, bits.ibackgroundcopyjob_enumfiles, bits/IBackgroundCopyJob::EnumFiles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.EnumFiles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob::EnumFiles


## -description


Retrieves an 
<a href="https://msdn.microsoft.com/831998ba-601c-43c4-ba27-faff741f8eb4">IEnumBackgroundCopyFiles</a> interface pointer that you use to 
<a href="https://msdn.microsoft.com/0e1fa024-4576-434c-bc5f-518d246b5faa">enumerate the files</a> in a job.


## -parameters




### -param pEnum [out]


<a href="https://msdn.microsoft.com/831998ba-601c-43c4-ba27-faff741f8eb4">IEnumBackgroundCopyFiles</a> interface pointer that you use to enumerate the files in the job. Release <i>ppEnumFiles</i> when done.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -see-also




<a href="https://msdn.microsoft.com/e8b73060-dff9-4ab3-8009-d2b41502fc1a">IBackgroundCopyManager::EnumJobs</a>



<a href="https://msdn.microsoft.com/831998ba-601c-43c4-ba27-faff741f8eb4">IEnumBackgroundCopyFiles</a>
 

 

