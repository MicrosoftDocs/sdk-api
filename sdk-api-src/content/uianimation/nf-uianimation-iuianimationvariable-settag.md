---
UID: NF:uianimation.IUIAnimationVariable.SetTag
title: IUIAnimationVariable::SetTag (uianimation.h)
description: Sets the tag for an animation variable.
helpviewer_keywords: ["IUIAnimationVariable interface [Windows Animation]","SetTag method","IUIAnimationVariable.SetTag","IUIAnimationVariable::SetTag","SetTag","SetTag method [Windows Animation]","SetTag method [Windows Animation]","IUIAnimationVariable interface","uianimation.iuianimationvariable_settag","uianimation/IUIAnimationVariable::SetTag"]
old-location: uianimation\iuianimationvariable_settag.htm
tech.root: UIAnimation
ms.assetid: 176b0047-cac8-474b-9126-fdab4bc41537
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariable interface [Windows Animation],SetTag method, IUIAnimationVariable.SetTag, IUIAnimationVariable::SetTag, SetTag, SetTag method [Windows Animation], SetTag method [Windows Animation],IUIAnimationVariable interface, uianimation.iuianimationvariable_settag, uianimation/IUIAnimationVariable::SetTag
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps \| UWP apps]
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
 - IUIAnimationVariable::SetTag
 - uianimation/IUIAnimationVariable::SetTag
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
 - IUIAnimationVariable.SetTag
---

# IUIAnimationVariable::SetTag


## -description

Sets the tag for an animation variable.

## -parameters

### -param object [in, optional]

The object portion of the tag.
            This parameter can be <b>NULL</b>.

### -param id [in]

The identifier portion  of the tag.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

A tag is a pairing of an integer identifier (<i>id</i>) with a COM object (<i>object</i>); it can be used by an application to identify an animation variable.          
         Because <b>NULL</b> is a valid object component of a tag, the <i>object</i> parameter can be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getvariablefromtag">IUIAnimationManager::GetVariableFromTag</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-gettag">IUIAnimationVariable::GetTag</a>