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

# PropSheet_IndexToPage macro


## -description


Takes the index of a property sheet page and returns its HPROPSHEETPAGE handle. You can use this macro or send the <a href="https://msdn.microsoft.com/b14b35ad-bae0-4461-a90f-e2bc5e2ccfc2">PSM_INDEXTOPAGE</a> message explicitly.


## -parameters




### -param hDlg

TBD


### -param i

TBD






#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet window.


#### - iPageIndex

Type: <b>int</b>

Zero-based index of the page.


## -see-also




<a href="https://msdn.microsoft.com/e93d4d3f-a046-4f2b-8eab-91bf33c7cd1d">PropSheet_PageToIndex</a>
 

 

