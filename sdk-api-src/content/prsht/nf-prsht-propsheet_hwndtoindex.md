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

# PropSheet_HwndToIndex macro


## -description


Takes a window handle of the property sheet page and returns its zero-based index. You can use this macro or send the <a href="https://msdn.microsoft.com/2eda4c95-95ed-4ebf-8245-c5b96aeb9075">PSM_HWNDTOINDEX</a> message explicitly.


## -parameters




### -param hDlg

TBD


### -param hwnd

TBD






#### - hPageDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the page's window.


#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet's window.


## -see-also




<a href="https://msdn.microsoft.com/9e1991dd-e451-4f2a-ac9f-069acb8e89c2">GetParent</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/b201025b-c468-4bfb-825b-63d59d1a62c8">PropSheet_GetCurrentPageHwnd</a>



<b>Reference</b>
 

 

