---
UID: NF:dcomp.IDCompositionDevice2.WaitForCommitCompletion
title: IDCompositionDevice2::WaitForCommitCompletion (dcomp.h)
author: windows-sdk-content
description: Waits for the composition engine to finish processing the previous call to the IDCompositionDevice2::Commit method.
old-location: directcomp\idcompositiondevice2_waitforcommitcompletion.htm
tech.root: directcomp
ms.assetid: 98C790BD-5C51-4A77-9DB4-51A263A4EC2A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionDevice2 interface [DirectComposition],WaitForCommitCompletion method, IDCompositionDevice2.WaitForCommitCompletion, IDCompositionDevice2::WaitForCommitCompletion, WaitForCommitCompletion, WaitForCommitCompletion method [DirectComposition], WaitForCommitCompletion method [DirectComposition],IDCompositionDevice2 interface, dcomp/IDCompositionDevice2::WaitForCommitCompletion, directcomp.idcompositiondevice2_waitforcommitcompletion
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDCompositionDevice2.WaitForCommitCompletion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice2::WaitForCommitCompletion


## -description


Waits for the composition engine to finish processing the previous call to the <a href="https://msdn.microsoft.com/8C24DE03-CF1E-4DC4-8C27-913DAD278579">IDCompositionDevice2::Commit</a> method. 


## -parameters






## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/0E5D0AEC-63A3-4A44-9A0B-D1E26789CAB0">IDCompositionDevice2</a>
 

 

