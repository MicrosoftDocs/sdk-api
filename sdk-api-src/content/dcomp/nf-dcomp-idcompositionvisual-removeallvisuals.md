---
UID: NF:dcomp.IDCompositionVisual.RemoveAllVisuals
title: IDCompositionVisual::RemoveAllVisuals (dcomp.h)
description: Removes all visuals from the children list of this visual.
helpviewer_keywords: ["IDCompositionVisual interface [DirectComposition]","RemoveAllVisuals method","IDCompositionVisual.RemoveAllVisuals","IDCompositionVisual::RemoveAllVisuals","RemoveAllVisuals","RemoveAllVisuals method [DirectComposition]","RemoveAllVisuals method [DirectComposition]","IDCompositionVisual interface","dcomp/IDCompositionVisual::RemoveAllVisuals","directcomp.idcompositionvisual_removeallvisuals"]
old-location: directcomp\idcompositionvisual_removeallvisuals.htm
tech.root: directcomp
ms.assetid: b3872d6a-f3f8-4343-b01d-6db5490abb13
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],RemoveAllVisuals method, IDCompositionVisual.RemoveAllVisuals, IDCompositionVisual::RemoveAllVisuals, RemoveAllVisuals, RemoveAllVisuals method [DirectComposition], RemoveAllVisuals method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::RemoveAllVisuals, directcomp.idcompositionvisual_removeallvisuals
f1_keywords:
- dcomp/IDCompositionVisual.RemoveAllVisuals
dev_langs:
- c++
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
- IDCompositionVisual.RemoveAllVisuals
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionVisual::RemoveAllVisuals


## -description


Removes all visuals from the children list of this visual.


## -parameters






## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method can be called even if this visual has no children. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createvisual">IDCompositionDevice::CreateVisual</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-addvisual">IDCompositionVisual::AddVisual</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-removevisual">IDCompositionVisual::RemoveVisual</a>
 

 

