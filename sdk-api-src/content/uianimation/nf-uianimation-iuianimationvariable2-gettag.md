---
UID: NF:uianimation.IUIAnimationVariable2.GetTag
title: IUIAnimationVariable2::GetTag (uianimation.h)
description: Gets the tag of the animation variable.
helpviewer_keywords: ["GetTag","GetTag method [Windows Animation]","GetTag method [Windows Animation]","IUIAnimationVariable2 interface","IUIAnimationVariable2 interface [Windows Animation]","GetTag method","IUIAnimationVariable2.GetTag","IUIAnimationVariable2::GetTag","uianimation.iuianimationvariable2_gettag","uianimation/IUIAnimationVariable2::GetTag"]
old-location: uianimation\iuianimationvariable2_gettag.htm
tech.root: UIAnimation
ms.assetid: 29E6CA4D-527D-4C9D-9E28-2E2C67516126
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Windows Animation], GetTag method [Windows Animation],IUIAnimationVariable2 interface, IUIAnimationVariable2 interface [Windows Animation],GetTag method, IUIAnimationVariable2.GetTag, IUIAnimationVariable2::GetTag, uianimation.iuianimationvariable2_gettag, uianimation/IUIAnimationVariable2::GetTag
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAnimation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAnimationVariable2::GetTag
 - uianimation/IUIAnimationVariable2::GetTag
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationVariable2.GetTag
---

# IUIAnimationVariable2::GetTag


## -description

Gets the tag of the animation variable.

## -parameters

### -param object [out, optional]

The object portion of the tag.

### -param id [out, optional]

The identifier portion of the tag.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

A tag is a pairing of an integer identifier (<i>id</i>) with a COM object (<i>object</i>); it can be used by an application to identify an animation variable.

The parameters are optional, so that the method can return both portions of the tag, or just the identifier or object portion.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>