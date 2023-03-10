---
UID: NF:dcomp.IDCompositionDevice.Commit
title: IDCompositionDevice::Commit (dcomp.h)
description: Commits all DirectComposition commands that are pending on this device. (IDCompositionDevice.Commit)
helpviewer_keywords: ["Commit","Commit method [DirectComposition]","Commit method [DirectComposition]","IDCompositionDevice interface","IDCompositionDevice interface [DirectComposition]","Commit method","IDCompositionDevice.Commit","IDCompositionDevice::Commit","dcomp/IDCompositionDevice::Commit","directcomp.idcompositiondevice_commit"]
old-location: directcomp\idcompositiondevice_commit.htm
tech.root: directcomp
ms.assetid: 49a6d33d-7454-44be-b8ca-602b247d4eab
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [DirectComposition], Commit method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],Commit method, IDCompositionDevice.Commit, IDCompositionDevice::Commit, dcomp/IDCompositionDevice::Commit, directcomp.idcompositiondevice_commit
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
 - IDCompositionDevice::Commit
 - dcomp/IDCompositionDevice::Commit
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
 - IDCompositionDevice.Commit
---

# IDCompositionDevice::Commit


## -description

Commits all DirectComposition commands that are pending on this device.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

Calls to DirectComposition methods are always batched and executed atomically as a single transaction. Calls take effect only when <b>IDCompositionDevice::Commit</b> is called, at which time all pending method calls for a device are executed at once. 

An application that uses multiple devices must call <b>Commit</b> for each device separately. However, because the composition engine processes the calls individually, the batch of commands might not take effect at the same time. 


#### Examples

For an example, see <a href="/windows/desktop/directcomp/how-to--build-a-visual-tree">How to Build a Simple Visual Tree</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>
