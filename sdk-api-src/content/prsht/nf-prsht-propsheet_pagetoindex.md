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

# PropSheet_PageToIndex macro


## -description


Takes the HPROPSHEETPAGE handle of a property sheet page and returns its zero-based index. You can use this macro or send the <a href="https://msdn.microsoft.com/f893b504-7b46-4bce-9598-79522825d43c">PSM_PAGETOINDEX</a> message explicitly.


## -parameters




### -param hDlg

TBD


### -param hpage

TBD






#### - hPage

Type: <b>HPROPSHEETPAGE</b>

HPROPSHEETPAGE handle to the property sheet page.


#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


## -see-also




<a href="https://msdn.microsoft.com/fb7ca67a-7dff-4e1d-a303-5da87d8bbd2b">CreatePropertySheetPage</a>



<a href="https://msdn.microsoft.com/c2b8b8c6-5225-486d-ba65-c87f116b974f">PropSheet_IndexToPage</a>



<b>Reference</b>
 

 

