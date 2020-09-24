---
UID: NF:dcomp.IDCompositionVisual.RemoveVisual
title: IDCompositionVisual::RemoveVisual (dcomp.h)
description: Removes a child visual from the children list of this visual.
helpviewer_keywords: ["IDCompositionVisual interface [DirectComposition]","RemoveVisual method","IDCompositionVisual.RemoveVisual","IDCompositionVisual::RemoveVisual","RemoveVisual","RemoveVisual method [DirectComposition]","RemoveVisual method [DirectComposition]","IDCompositionVisual interface","dcomp/IDCompositionVisual::RemoveVisual","directcomp.idcompositionvisual_removevisual"]
old-location: directcomp\idcompositionvisual_removevisual.htm
tech.root: directcomp
ms.assetid: d77161b1-cb35-40a7-a51c-4b44ea320e78
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],RemoveVisual method, IDCompositionVisual.RemoveVisual, IDCompositionVisual::RemoveVisual, RemoveVisual, RemoveVisual method [DirectComposition], RemoveVisual method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::RemoveVisual, directcomp.idcompositionvisual_removevisual
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
 - IDCompositionVisual::RemoveVisual
 - dcomp/IDCompositionVisual::RemoveVisual
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
 - IDCompositionVisual.RemoveVisual
---

# IDCompositionVisual::RemoveVisual


## -description

Removes a child visual from the children list of this visual.

## -parameters

### -param visual [in]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>*</b>

The child visual to remove from the children list. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

The child visual is removed from the list of children. The order of the remaining child visuals is not changed.

This method fails if <i>visual</i> is not a child of the parent visual.

## -see-also

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createvisual">IDCompositionDevice::CreateVisual</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-addvisual">IDCompositionVisual::AddVisual</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-removeallvisuals">IDCompositionVisual::RemoveAllVisuals</a>