---
UID: NF:dcomp.IDCompositionDevice.CreateEffectGroup
title: IDCompositionDevice::CreateEffectGroup (dcomp.h)
author: windows-sdk-content
description: Creates an object that represents multiple effects to be applied to a visual subtree.
old-location: directcomp\idcompositiondevice_createeffectgroup.htm
tech.root: directcomp
ms.assetid: FCF3AACB-F61D-43D4-BAFB-D9453C745956
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateEffectGroup, CreateEffectGroup method [DirectComposition], CreateEffectGroup method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateEffectGroup method, IDCompositionDevice.CreateEffectGroup, IDCompositionDevice::CreateEffectGroup, dcomp/IDCompositionDevice::CreateEffectGroup, directcomp.idcompositiondevice_createeffectgroup
ms.topic: method
f1_keywords: ["dcomp/IDCompositionDevice.CreateEffectGroup"]
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
 - IDCompositionDevice.CreateEffectGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionDevice::CreateEffectGroup


## -description


Creates an object that represents multiple effects to be applied to a visual subtree.


## -parameters




### -param effectGroup [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositioneffectgroup">IDCompositionEffectGroup</a>**</b>

The new effect group object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



An effect group enables an application to apply multiple effects to a single visual subtree. 

A new effect group has a default opacity value of 1.0 and no 3D transformations.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">IDCompositionVisual::SetEffect</a>
 

 

