---
UID: NF:dcomp.IDCompositionDevice2.Commit
title: IDCompositionDevice2::Commit (dcomp.h)
description: Commits all DirectComposition commands that are pending on this device. (IDCompositionDevice2.Commit)
helpviewer_keywords: ["Commit","Commit method [DirectComposition]","Commit method [DirectComposition]","IDCompositionDevice2 interface","IDCompositionDevice2 interface [DirectComposition]","Commit method","IDCompositionDevice2.Commit","IDCompositionDevice2::Commit","dcomp/IDCompositionDevice2::Commit","directcomp.idcompositiondevice2_commit"]
old-location: directcomp\idcompositiondevice2_commit.htm
tech.root: directcomp
ms.assetid: 8C24DE03-CF1E-4DC4-8C27-913DAD278579
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [DirectComposition], Commit method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],Commit method, IDCompositionDevice2.Commit, IDCompositionDevice2::Commit, dcomp/IDCompositionDevice2::Commit, directcomp.idcompositiondevice2_commit
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionDevice2::Commit
 - dcomp/IDCompositionDevice2::Commit
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
 - IDCompositionDevice2.Commit
---

# IDCompositionDevice2::Commit


## -description

Commits all DirectComposition commands that are pending on this device.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> 
       error code. See 
       <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a> for a 
       list of error codes.

## -remarks

Calls to DirectComposition methods are always batched and executed atomically as 
    a single transaction. Calls take effect only when 
    <b>IDCompositionDevice2::Commit</b> is 
    called, at which time all pending method calls for a device are executed at once.

An application that uses multiple devices must call 
    <b>Commit</b> for each device separately. 
    However, because the composition engine processes the calls individually, the batch of commands might not take 
    effect at the same time.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>
