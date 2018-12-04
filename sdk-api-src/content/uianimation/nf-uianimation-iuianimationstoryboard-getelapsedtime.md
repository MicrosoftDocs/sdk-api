---
UID: NF:uianimation.IUIAnimationStoryboard.GetElapsedTime
title: IUIAnimationStoryboard::GetElapsedTime
author: windows-sdk-content
description: Gets the time that has elapsed since the storyboard started playing.
old-location: uianimation\iuianimationstoryboard_getelapsedtime.htm
tech.root: UIAnimation
ms.assetid: 901afd34-03cc-4421-a467-9d096e1458fe
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetElapsedTime, GetElapsedTime method [Windows Animation], GetElapsedTime method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],GetElapsedTime method, IUIAnimationStoryboard.GetElapsedTime, IUIAnimationStoryboard::GetElapsedTime, uianimation.iuianimationstoryboard_getelapsedtime, uianimation/IUIAnimationStoryboard::GetElapsedTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationStoryboard.GetElapsedTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationStoryboard::GetElapsedTime


## -description


Gets the time that has elapsed since the storyboard started playing.


## -parameters




### -param elapsedTime [out]

The elapsed time.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.            
             See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.

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




<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/8ee9a17f-c57c-49df-950d-491e05ba8768">IUIAnimationStoryboard::GetStatus</a>



<a href="https://msdn.microsoft.com/02830092-0070-44dc-8db2-239941134473">UI_ANIMATION_STORYBOARD_STATUS</a>
 

 

