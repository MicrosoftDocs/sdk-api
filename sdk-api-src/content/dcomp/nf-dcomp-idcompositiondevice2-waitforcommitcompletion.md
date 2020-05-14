---
UID: NF:dcomp.IDCompositionDevice2.WaitForCommitCompletion
title: IDCompositionDevice2::WaitForCommitCompletion (dcomp.h)
description: Waits for the composition engine to finish processing the previous call to the IDCompositionDevice2::Commit method.helpviewer_keywords: ["IDCompositionDevice2 interface [DirectComposition]","WaitForCommitCompletion method","IDCompositionDevice2.WaitForCommitCompletion","IDCompositionDevice2::WaitForCommitCompletion","WaitForCommitCompletion","WaitForCommitCompletion method [DirectComposition]","WaitForCommitCompletion method [DirectComposition]","IDCompositionDevice2 interface","dcomp/IDCompositionDevice2::WaitForCommitCompletion","directcomp.idcompositiondevice2_waitforcommitcompletion"]
old-location: directcomp\idcompositiondevice2_waitforcommitcompletion.htm
tech.root: directcomp
ms.assetid: 98C790BD-5C51-4A77-9DB4-51A263A4EC2A
ms.date: 12/05/2018
ms.keywords: IDCompositionDevice2 interface [DirectComposition],WaitForCommitCompletion method, IDCompositionDevice2.WaitForCommitCompletion, IDCompositionDevice2::WaitForCommitCompletion, WaitForCommitCompletion, WaitForCommitCompletion method [DirectComposition], WaitForCommitCompletion method [DirectComposition],IDCompositionDevice2 interface, dcomp/IDCompositionDevice2::WaitForCommitCompletion, directcomp.idcompositiondevice2_waitforcommitcompletion
f1_keywords:
- dcomp/IDCompositionDevice2.WaitForCommitCompletion
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionDevice2::WaitForCommitCompletion


## -description


Waits for the composition engine to finish processing the previous call to the <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice2-commit">IDCompositionDevice2::Commit</a> method. 


## -parameters






## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>
 

 

