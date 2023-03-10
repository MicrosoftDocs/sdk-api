---
UID: NF:uianimation.IUIAnimationStoryboard.SetTag
title: IUIAnimationStoryboard::SetTag (uianimation.h)
description: Sets the tag for the storyboard. (IUIAnimationStoryboard.SetTag)
helpviewer_keywords: ["IUIAnimationStoryboard interface [Windows Animation]","SetTag method","IUIAnimationStoryboard.SetTag","IUIAnimationStoryboard::SetTag","SetTag","SetTag method [Windows Animation]","SetTag method [Windows Animation]","IUIAnimationStoryboard interface","uianimation.iuianimationstoryboard_settag","uianimation/IUIAnimationStoryboard::SetTag"]
old-location: uianimation\iuianimationstoryboard_settag.htm
tech.root: UIAnimation
ms.assetid: ade41b03-9194-4b1a-a672-32bb48a2f5ba
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboard interface [Windows Animation],SetTag method, IUIAnimationStoryboard.SetTag, IUIAnimationStoryboard::SetTag, SetTag, SetTag method [Windows Animation], SetTag method [Windows Animation],IUIAnimationStoryboard interface, uianimation.iuianimationstoryboard_settag, uianimation/IUIAnimationStoryboard::SetTag
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
 - IUIAnimationStoryboard::SetTag
 - uianimation/IUIAnimationStoryboard::SetTag
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
 - IUIAnimationStoryboard.SetTag
---

# IUIAnimationStoryboard::SetTag


## -description

Sets the tag for the storyboard.

## -parameters

### -param object [in, optional]

The object portion of the tag.        
            This parameter can be <b>NULL</b>.

### -param id [in]

The identifier portion of the tag.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_STORYBOARD_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The storyboard is currently in the schedule.

</td>
</tr>
</table>

## -remarks

A tag is a pairing of an integer identifier (<i>id</i>) with a COM object (<i>object</i>); it can be used by an application to identify a storyboard.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getstoryboardfromtag">IUIAnimationManager::GetStoryboardFromTag</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-gettag">IUIAnimationStoryboard::GetTag</a>
