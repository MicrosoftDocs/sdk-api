---
UID: NF:dcomp.IDCompositionDevice.WaitForCommitCompletion
title: IDCompositionDevice::WaitForCommitCompletion (dcomp.h)
description: Waits for the composition engine to finish processing the previous call to the IDCompositionDevice::Commit method.
helpviewer_keywords: ["IDCompositionDevice interface [DirectComposition]","WaitForCommitCompletion method","IDCompositionDevice.WaitForCommitCompletion","IDCompositionDevice::WaitForCommitCompletion","WaitForCommitCompletion","WaitForCommitCompletion method [DirectComposition]","WaitForCommitCompletion method [DirectComposition]","IDCompositionDevice interface","dcomp/IDCompositionDevice::WaitForCommitCompletion","directcomp.idcompositiondevice_waitforcommitcompletion"]
old-location: directcomp\idcompositiondevice_waitforcommitcompletion.htm
tech.root: directcomp
ms.assetid: C921AC68-492C-4E29-876C-8857D5475B1D
ms.date: 12/05/2018
ms.keywords: IDCompositionDevice interface [DirectComposition],WaitForCommitCompletion method, IDCompositionDevice.WaitForCommitCompletion, IDCompositionDevice::WaitForCommitCompletion, WaitForCommitCompletion, WaitForCommitCompletion method [DirectComposition], WaitForCommitCompletion method [DirectComposition],IDCompositionDevice interface, dcomp/IDCompositionDevice::WaitForCommitCompletion, directcomp.idcompositiondevice_waitforcommitcompletion
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionDevice::WaitForCommitCompletion
 - dcomp/IDCompositionDevice::WaitForCommitCompletion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDevice.WaitForCommitCompletion
---

# IDCompositionDevice::WaitForCommitCompletion


## -description

Waits for the composition engine to finish processing the previous call to the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-commit">IDCompositionDevice::Commit</a> method.



## -returns

If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>
