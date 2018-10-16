---
UID: NF:dcomp.IDCompositionColorMatrixEffect.SetMatrix
title: IDCompositionColorMatrixEffect::SetMatrix
author: windows-sdk-content
description: Sets the matrix used by the effect to multiply the RGBA values of the image.
old-location: directcomp\idcompositioncolormatrixeffect_setmatrix.htm
tech.root: directcomp
ms.assetid: 1EE0C9B6-6309-40A3-AE80-A47C45BBA536
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IDCompositionColorMatrixEffect interface [DirectComposition],SetMatrix method, IDCompositionColorMatrixEffect.SetMatrix, IDCompositionColorMatrixEffect::SetMatrix, SetMatrix, SetMatrix method [DirectComposition], SetMatrix method [DirectComposition],IDCompositionColorMatrixEffect interface, dcomp/IDCompositionColorMatrixEffect::SetMatrix, directcomp.idcompositioncolormatrixeffect_setmatrix
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDCompositionColorMatrixEffect.SetMatrix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionColorMatrixEffect::SetMatrix


## -description


Sets the matrix used by the effect to multiply the RGBA values of the image.


## -parameters




### -param matrix [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/c6f57691-1530-e57a-c1b4-b68b4d8967e3">D2D1_MATRIX_5X4_F</a></b>

The matrix used by the effect to multiply the RGBA values of the image. The matrix is column major and is applied as shown in the following equation:
          

<img alt="Matrix equation" src="images/color_matrix_formula.png"/>

## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/75528E11-D041-4192-833A-31679316DF76">IDCompositionColorMatrixEffect</a>
 

 

