---
UID: NF:uianimation.IUIAnimationStoryboard2.SetTag
title: IUIAnimationStoryboard2::SetTag (uianimation.h)
description: Sets the tag for the storyboard. (IUIAnimationStoryboard2.SetTag)
helpviewer_keywords: ["IUIAnimationStoryboard2 interface [Windows Animation]","SetTag method","IUIAnimationStoryboard2.SetTag","IUIAnimationStoryboard2::SetTag","SetTag","SetTag method [Windows Animation]","SetTag method [Windows Animation]","IUIAnimationStoryboard2 interface","uianimation.iuianimationstoryboard2_settag","uianimation/IUIAnimationStoryboard2::SetTag"]
old-location: uianimation\iuianimationstoryboard2_settag.htm
tech.root: UIAnimation
ms.assetid: 9BEB2BF7-55F7-43F7-822C-CB4AC6F29E32
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboard2 interface [Windows Animation],SetTag method, IUIAnimationStoryboard2.SetTag, IUIAnimationStoryboard2::SetTag, SetTag, SetTag method [Windows Animation], SetTag method [Windows Animation],IUIAnimationStoryboard2 interface, uianimation.iuianimationstoryboard2_settag, uianimation/IUIAnimationStoryboard2::SetTag
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
 - IUIAnimationStoryboard2::SetTag
 - uianimation/IUIAnimationStoryboard2::SetTag
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
 - IUIAnimationStoryboard2.SetTag
---

# IUIAnimationStoryboard2::SetTag


## -description

Sets the tag for the storyboard.

## -parameters

### -param object [in, optional]

The object portion of the tag.        
            This parameter can be NULL.

### -param id [in]

The identifier portion of the tag.

## -returns

Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

A tag is a pairing of an integer identifier (<i>id</i>) with a COM object (<i>object</i>). It can be used by an application to identify a storyboard.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-getstoryboardfromtag">IUIAnimationManager2::GetStoryboardFromTag</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-gettag">IUIAnimationStoryboard2::GetTag</a>
