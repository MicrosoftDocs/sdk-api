---
UID: NF:uianimation.IUIAnimationStoryboard2.GetTag
title: IUIAnimationStoryboard2::GetTag (uianimation.h)
description: Gets the tag for a storyboard. (IUIAnimationStoryboard2.GetTag)
helpviewer_keywords: ["GetTag","GetTag method [Windows Animation]","GetTag method [Windows Animation]","IUIAnimationStoryboard2 interface","IUIAnimationStoryboard2 interface [Windows Animation]","GetTag method","IUIAnimationStoryboard2.GetTag","IUIAnimationStoryboard2::GetTag","uianimation.iuianimationstoryboard2_gettag","uianimation/IUIAnimationStoryboard2::GetTag"]
old-location: uianimation\iuianimationstoryboard2_gettag.htm
tech.root: UIAnimation
ms.assetid: A73D5003-FC28-4A79-B157-3D0D2E0DEB3D
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Windows Animation], GetTag method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],GetTag method, IUIAnimationStoryboard2.GetTag, IUIAnimationStoryboard2::GetTag, uianimation.iuianimationstoryboard2_gettag, uianimation/IUIAnimationStoryboard2::GetTag
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
 - IUIAnimationStoryboard2::GetTag
 - uianimation/IUIAnimationStoryboard2::GetTag
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
 - IUIAnimationStoryboard2.GetTag
---

# IUIAnimationStoryboard2::GetTag


## -description

Gets the tag for a storyboard.

## -parameters

### -param object [out, optional]

The object portion of the tag.

### -param id [out, optional]

The identifier portion of the tag.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_VALUE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The storyboard tag was not set.

</td>
</tr>
</table>

## -remarks

A tag is a pairing of an integer identifier (<i>id</i>) with a COM object (<i>object</i>); it can be used by an application to identify a storyboard.

This method can return the identifier, the object, or both portions of the tag.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-getstoryboardfromtag">IUIAnimationManager2::GetStoryboardFromTag</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-settag">IUIAnimationStoryboard2::SetTag</a>
