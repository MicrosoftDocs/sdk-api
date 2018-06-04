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

# PropSheet_SetHeaderTitle macro


## -description


Sets the title text for the header of a wizard's interior page. You can use this macro or send the <a href="https://msdn.microsoft.com/19d4badf-d99d-4a28-92d4-33bcf5d23944">PSM_SETHEADERTITLE</a> message explicitly.


## -parameters




### -param hDlg

TBD


### -param index

TBD


### -param lpszText

TBD






#### - hWizardDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the wizard's window.


#### - iPageIndex

Type: <b>int</b>

Zero-based index of the page.


#### - pszHeaderTitle

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

New header title.


## -remarks



If you specify the current page, it will immediately be repainted to display the new title.



