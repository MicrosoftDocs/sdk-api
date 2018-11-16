---
UID: NF:uianimation.IUIAnimationVariable2.GetTag
title: IUIAnimationVariable2::GetTag
author: windows-sdk-content
description: Gets the tag of the animation variable.
old-location: uianimation\iuianimationvariable2_gettag.htm
tech.root: UIAnimation
ms.assetid: 29E6CA4D-527D-4C9D-9E28-2E2C67516126
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetTag, GetTag method [Windows Animation], GetTag method [Windows Animation],IUIAnimationVariable2 interface, IUIAnimationVariable2 interface [Windows Animation],GetTag method, IUIAnimationVariable2.GetTag, IUIAnimationVariable2::GetTag, uianimation.iuianimationvariable2_gettag, uianimation/IUIAnimationVariable2::GetTag
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationVariable2.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uianimation.h
: 
- IUIAnimationVariable2.GetTag
: 
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



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



A tag is a pairing of an integer identifier (<i>id</i>) with a COM object (<i>object</i>); it can be used by an application to identify an animation variable.

The parameters are optional, so that the method can return both portions of the tag, or just the identifier or object portion.




## -see-also




<a href="https://msdn.microsoft.com/A676EF27-B59D-4D2D-AD5B-8F46EE337E69">IUIAnimationVariable2</a>
 

 

