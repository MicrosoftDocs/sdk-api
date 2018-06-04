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

# PropSheet_SetFinishText macro


## -description


Sets the text of the Finish button in a wizard, shows and enables the button, and hides the Next and Back buttons. You can use this macro or send the <a href="https://msdn.microsoft.com/fa89c6d7-9ab7-4e7c-ba08-d665420492a3">PSM_SETFINISHTEXT</a> message explicitly.


## -parameters




### -param hDlg

TBD


### -param lpszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

Pointer to the new text for the Finish button.


#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Window handle (HWND) of the wizard property sheet.


## -remarks



By default, the Finish button does not have a keyboard accelerator. You can create a keyboard accelerator with this macro by including an ampersand (&amp;) in the text string that you assign to <i>lpszText</i>. For example, "&amp;Finish" defines F as the accelerator key.



