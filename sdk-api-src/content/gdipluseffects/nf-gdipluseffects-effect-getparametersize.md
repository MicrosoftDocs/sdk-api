---
UID: NF:gdipluseffects.Effect.GetParameterSize
title: Effect::GetParameterSize (gdipluseffects.h)
description: The Effect::GetParameterSize method gets the total size, in bytes, of the parameters currently set for this Effect. The Effect::GetParameterSize method is usually called on an object that is an instance of a descendant of the Effect class.
helpviewer_keywords: ["Effect class [GDI+]","GetParameterSize method","Effect.GetParameterSize","Effect::GetParameterSize","GetParameterSize","GetParameterSize method [GDI+]","GetParameterSize method [GDI+]","Effect class","_gdiplus_CLASS_Effect_GetParameterSize_","gdiplus._gdiplus_CLASS_Effect_GetParameterSize_"]
old-location: gdiplus\_gdiplus_CLASS_Effect_GetParameterSize_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\effectclass\effectmethods\getparametersize.htm
ms.date: 12/05/2018
ms.keywords: Effect class [GDI+],GetParameterSize method, Effect.GetParameterSize, Effect::GetParameterSize, GetParameterSize, GetParameterSize method [GDI+], GetParameterSize method [GDI+],Effect class, _gdiplus_CLASS_Effect_GetParameterSize_, gdiplus._gdiplus_CLASS_Effect_GetParameterSize_
req.header: gdipluseffects.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
f1_keywords:
 - Effect::GetParameterSize
 - gdipluseffects/Effect::GetParameterSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Effect.GetParameterSize
---

# Effect::GetParameterSize


## -description

The <b>Effect::GetParameterSize</b> method  gets the total size, in bytes, of the parameters currently set for this <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-effect">Effect</a>. The <b>Effect::GetParameterSize</b> method is usually called on an object that is an instance of a descendant of the <b>Effect</b> class.

## -parameters

### -param size [out]

Type: <b>UINT*</b>

Pointer to a UINT that receives the total size of the parameters.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-effect">Effect</a>



<a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-redeyecorrection-setparameters">SetParameters</a>