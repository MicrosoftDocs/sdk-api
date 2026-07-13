---
UID: NF:uianimation.IUIAnimationManager2.GetStoryboardFromTag
title: IUIAnimationManager2::GetStoryboardFromTag (uianimation.h)
description: Gets the storyboard with the specified tag. (IUIAnimationManager2.GetStoryboardFromTag)
helpviewer_keywords: ["GetStoryboardFromTag","GetStoryboardFromTag method [Windows Animation]","GetStoryboardFromTag method [Windows Animation]","IUIAnimationManager2 interface","IUIAnimationManager2 interface [Windows Animation]","GetStoryboardFromTag method","IUIAnimationManager2.GetStoryboardFromTag","IUIAnimationManager2::GetStoryboardFromTag","uianimation.iuianimationmanager2_getstoryboardfromtag","uianimation/IUIAnimationManager2::GetStoryboardFromTag"]
old-location: uianimation\iuianimationmanager2_getstoryboardfromtag.htm
tech.root: UIAnimation
ms.assetid: C7B11A34-E5FB-40D7-A655-29D28ECF4068
ms.date: 12/05/2018
ms.keywords: GetStoryboardFromTag, GetStoryboardFromTag method [Windows Animation], GetStoryboardFromTag method [Windows Animation],IUIAnimationManager2 interface, IUIAnimationManager2 interface [Windows Animation],GetStoryboardFromTag method, IUIAnimationManager2.GetStoryboardFromTag, IUIAnimationManager2::GetStoryboardFromTag, uianimation.iuianimationmanager2_getstoryboardfromtag, uianimation/IUIAnimationManager2::GetStoryboardFromTag
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
 - IUIAnimationManager2::GetStoryboardFromTag
 - uianimation/IUIAnimationManager2::GetStoryboardFromTag
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
 - IUIAnimationManager2.GetStoryboardFromTag
---

# IUIAnimationManager2::GetStoryboardFromTag


## -description

Gets the storyboard with the specified tag.

## -parameters

### -param object [in, optional]

The object portion of the tag.
            This parameter can be NULL.

### -param id [in]

The identifier portion of the tag.

### -param storyboard [out]

The storyboard that matches the specified tag, or <b>NULL</b> if no match is found.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

A tag is a pairing of an integer identifier (<i>id</i>) with a COM object (<i>object</i>). An application can use tags to identify animation variables and storyboards. NULL is a valid object component of a tag; therefore, the <i>object</i> parameter can be NULL.

Tags are not necessarily unique; this method returns UI_E_AMBIGUOUS_MATCH if more than one storyboard exists with the specified tag.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">IUIAnimationManager2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-gettag">IUIAnimationStoryboard::GetTag
      </a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-settag">IUIAnimationStoryboard::SetTag
      </a>
