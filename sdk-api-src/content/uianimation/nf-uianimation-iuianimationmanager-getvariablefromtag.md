---
UID: NF:uianimation.IUIAnimationManager.GetVariableFromTag
title: IUIAnimationManager::GetVariableFromTag (uianimation.h)
description: Gets the animation variable with the specified tag. (IUIAnimationManager.GetVariableFromTag)
helpviewer_keywords: ["GetVariableFromTag","GetVariableFromTag method [Windows Animation]","GetVariableFromTag method [Windows Animation]","IUIAnimationManager interface","IUIAnimationManager interface [Windows Animation]","GetVariableFromTag method","IUIAnimationManager.GetVariableFromTag","IUIAnimationManager::GetVariableFromTag","uianimation.iuianimationmanager_getvariablefromtag","uianimation/IUIAnimationManager::GetVariableFromTag"]
old-location: uianimation\iuianimationmanager_getvariablefromtag.htm
tech.root: UIAnimation
ms.assetid: 611c5341-f225-461d-9718-a2432d796764
ms.date: 12/05/2018
ms.keywords: GetVariableFromTag, GetVariableFromTag method [Windows Animation], GetVariableFromTag method [Windows Animation],IUIAnimationManager interface, IUIAnimationManager interface [Windows Animation],GetVariableFromTag method, IUIAnimationManager.GetVariableFromTag, IUIAnimationManager::GetVariableFromTag, uianimation.iuianimationmanager_getvariablefromtag, uianimation/IUIAnimationManager::GetVariableFromTag
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
 - IUIAnimationManager::GetVariableFromTag
 - uianimation/IUIAnimationManager::GetVariableFromTag
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
 - IUIAnimationManager.GetVariableFromTag
---

# IUIAnimationManager::GetVariableFromTag


## -description

Gets the animation variable with the specified tag.

## -parameters

### -param object [in, optional]

The object portion of the tag.
            This parameter can be <b>NULL</b>.

### -param id [in]

The identifier portion of the tag.

### -param variable [out]

The animation variable that matches the specified tag, or <b>NULL</b> if no match is found.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

A tag is a pairing of an integer identifier (<i>id</i>) with a COM object (<i>object</i>). An application can use tags to identify animation variables and storyboards. <b>NULL</b> is a valid object component of a tag; therefore, the <i>object</i> parameter can be <b>NULL</b>.

Tags are not necessarily unique; this method returns <b>UI_E_AMBIGUOUS_MATCH</b> if more than one animation variable exists with the specified tag.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-gettag">IUIAnimationVariable::GetTag</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-settag">IUIAnimationVariable::SetTag</a>
