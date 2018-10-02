---
UID: NF:dcomp.IDCompositionColorMatrixEffect.SetMatrixElement(int,int,IDCompositionAnimation)
title: IDCompositionColorMatrixEffect::SetMatrixElement(int,int,IDCompositionAnimation)
author: windows-sdk-content
description: Sets an element of the color matrix.
old-location: directcomp\idcompositioncolormatrixeffect_setmatrixelement.htm
tech.root: directcomp
ms.assetid: 4F78FA9F-8115-4D60-B119-F60968AAB1D4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDCompositionColorMatrixEffect interface [DirectComposition],SetMatrixElement method, IDCompositionColorMatrixEffect.SetMatrixElement, IDCompositionColorMatrixEffect.SetMatrixElement(int,int,IDCompositionAnimation), IDCompositionColorMatrixEffect::SetMatrixElement, IDCompositionColorMatrixEffect::SetMatrixElement(int,int,IDCompositionAnimation), SetMatrixElement, SetMatrixElement method [DirectComposition], SetMatrixElement method [DirectComposition],IDCompositionColorMatrixEffect interface, dcomp/IDCompositionColorMatrixEffect::SetMatrixElement, directcomp.idcompositioncolormatrixeffect_setmatrixelement
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
 - IDCompositionColorMatrixEffect.SetMatrixElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionColorMatrixEffect::SetMatrixElement(int,int,IDCompositionAnimation)


## -description


Sets an element of the color matrix.


## -parameters




### -param row [in]

Type: <b>int</b>

The row of the element.


### -param column [in]

Type: <b>int</b>

The column of the element.


### -param animation

TBD




#### - value [in]

Type: <b>float</b>

The new value of the element.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/75528E11-D041-4192-833A-31679316DF76">IDCompositionColorMatrixEffect</a>
 

 

