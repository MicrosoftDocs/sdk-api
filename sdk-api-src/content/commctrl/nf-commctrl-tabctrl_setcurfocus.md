---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# TabCtrl_SetCurFocus macro


## -description


Sets the focus to a specified tab in a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/bcbd5f26-b54e-492b-aff3-357b8ae23969">TCM_SETCURFOCUS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


### -param i

TBD






#### - iItem

Type: <b>int</b>

Zero-based index of the tab that gets the focus. 


## -remarks



If the tab control has the <a href="Tab_Control_Styles.htm">TCS_BUTTONS</a> style (button mode), the tab with the focus may be different from the selected tab. For example, when a tab is selected, the user can press the arrow keys to set the focus to a different tab without changing the selected tab. In button mode, the <b>TabCtrl_SetCurFocus</b> macro sets the input focus to the button associated with the specified tab, but it does not change the selected tab. 

If the tab control does not have the <a href="Tab_Control_Styles.htm">TCS_BUTTONS</a> style, changing the focus also changes the selected tab. In this case, the tab control sends the <a href="https://msdn.microsoft.com/ec7b1bd3-8932-4418-9eed-ecb7c748e4dd">TCN_SELCHANGING</a> and <a href="https://msdn.microsoft.com/f40e30f6-169b-4381-a300-12c3befb5fc5">TCN_SELCHANGE</a> notification codes to its parent window. 




## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/ae6ee159-c769-41d6-b0bb-2a9ade4c0e71">TCM_GETCURFOCUS</a>



<a href="https://msdn.microsoft.com/c177f904-8c6e-4312-a783-1e42fc01a430">TabCtrl_GetCurFocus</a>
 

 

