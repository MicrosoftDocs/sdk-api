---
UID: NF:uianimation.IUIAnimationStoryboard.GetElapsedTime
title: IUIAnimationStoryboard::GetElapsedTime (uianimation.h)
description: Gets the time that has elapsed since the storyboard started playing. (IUIAnimationStoryboard.GetElapsedTime)
helpviewer_keywords: ["GetElapsedTime","GetElapsedTime method [Windows Animation]","GetElapsedTime method [Windows Animation]","IUIAnimationStoryboard interface","IUIAnimationStoryboard interface [Windows Animation]","GetElapsedTime method","IUIAnimationStoryboard.GetElapsedTime","IUIAnimationStoryboard::GetElapsedTime","uianimation.iuianimationstoryboard_getelapsedtime","uianimation/IUIAnimationStoryboard::GetElapsedTime"]
old-location: uianimation\iuianimationstoryboard_getelapsedtime.htm
tech.root: UIAnimation
ms.assetid: 901afd34-03cc-4421-a467-9d096e1458fe
ms.date: 12/05/2018
ms.keywords: GetElapsedTime, GetElapsedTime method [Windows Animation], GetElapsedTime method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],GetElapsedTime method, IUIAnimationStoryboard.GetElapsedTime, IUIAnimationStoryboard::GetElapsedTime, uianimation.iuianimationstoryboard_getelapsedtime, uianimation/IUIAnimationStoryboard::GetElapsedTime
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
 - IUIAnimationStoryboard::GetElapsedTime
 - uianimation/IUIAnimationStoryboard::GetElapsedTime
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
 - IUIAnimationStoryboard.GetElapsedTime
---

# IUIAnimationStoryboard::GetElapsedTime


## -description

Gets the time that has elapsed since the storyboard started playing.

## -parameters

### -param elapsedTime [out]

The elapsed time.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.            
             See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_STORYBOARD_NOT_PLAYING</b></dt>
</dl>
</td>
<td width="60%">
The storyboard is not playing.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-getstatus">IUIAnimationStoryboard::GetStatus</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_STATUS</a>
