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

# PropSheet_SetCurSel macro


## -description


Activates the specified page in a property sheet. You can use this macro or send the <a href="https://msdn.microsoft.com/800aadde-cabc-424e-8e63-60fc7ce952d7">PSM_SETCURSEL</a> message explicitly.


## -parameters




### -param hDlg

TBD


### -param hpage

Type: <b>HPROPSHEETPAGE</b>

Handle to the page to activate. An application can specify the index or the handle, or both. If both are specified, <i>hpage</i> takes precedence.


### -param index

Type: <b>UINT</b>

Zero-based index of the page. An application can specify the index or the handle, or both. If both are specified, <i>hpage</i> takes precedence.


#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


## -remarks



The window that is losing the activation receives the <a href="https://msdn.microsoft.com/470cd6ff-73ad-451a-a861-4d3324a8a8db">PSN_KILLACTIVE</a> notification code, and the window that is gaining the activation receives the <a href="https://msdn.microsoft.com/0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463">PSN_SETACTIVE</a> notification code.



