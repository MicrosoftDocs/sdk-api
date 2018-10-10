---
UID: NF:dcomp.IDCompositionDevice.WaitForCommitCompletion
title: IDCompositionDevice::WaitForCommitCompletion
author: windows-sdk-content
description: Waits for the composition engine to finish processing the previous call to the IDCompositionDevice::Commit method.
old-location: directcomp\idcompositiondevice_waitforcommitcompletion.htm
tech.root: directcomp
ms.assetid: C921AC68-492C-4E29-876C-8857D5475B1D
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IDCompositionDevice interface [DirectComposition],WaitForCommitCompletion method, IDCompositionDevice.WaitForCommitCompletion, IDCompositionDevice::WaitForCommitCompletion, WaitForCommitCompletion, WaitForCommitCompletion method [DirectComposition], WaitForCommitCompletion method [DirectComposition],IDCompositionDevice interface, dcomp/IDCompositionDevice::WaitForCommitCompletion, directcomp.idcompositiondevice_waitforcommitcompletion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDevice.WaitForCommitCompletion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice::WaitForCommitCompletion


## -description


Waits for the composition engine to finish processing the previous call to the <a href="https://msdn.microsoft.com/49a6d33d-7454-44be-b8ca-602b247d4eab">IDCompositionDevice::Commit</a> method. 


## -parameters






## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a>
 

 

