---
UID: NF:uianimation.IUIAnimationStoryboard2.GetElapsedTime
title: IUIAnimationStoryboard2::GetElapsedTime
author: windows-driver-content
description: Gets the time that has elapsed since the storyboard started playing.
old-location: uianimation\iuianimationstoryboard2_getelapsedtime.htm
old-project: UIAnimation
ms.assetid: 014F8A6A-345A-4DA7-8002-20A4683BB3B6
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetElapsedTime, GetElapsedTime method [Windows Animation], GetElapsedTime method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],GetElapsedTime method, IUIAnimationStoryboard2.GetElapsedTime, IUIAnimationStoryboard2::GetElapsedTime, uianimation.iuianimationstoryboard2_getelapsedtime, uianimation/IUIAnimationStoryboard2::GetElapsedTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps | UWP apps]
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
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationStoryboard2.GetElapsedTime
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboard2::GetElapsedTime


## -description



      Gets the time that has elapsed since the storyboard started playing.


## -parameters




### -param elapsedTime [out]


            The elapsed time.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.

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




<a href="https://msdn.microsoft.com/507B6C2B-92C6-4AEB-82D5-3F14A332D41F">IUIAnimationStoryboard2</a>



<a href="https://msdn.microsoft.com/1694B720-891A-4214-A009-6AA722E5B83D">
      IUIAnimationStoryboard2::GetStatus</a>



<a href="https://msdn.microsoft.com/02830092-0070-44dc-8db2-239941134473">
      UI_ANIMATION_STORYBOARD_STATUS</a>
 

 

