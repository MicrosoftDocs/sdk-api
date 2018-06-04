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

# PropSheet_SetHeaderSubTitle macro


## -description


Sets the subtitle text for the header of a wizard's interior page. You can use this macro or send the <a href="https://msdn.microsoft.com/6ef3017b-8a20-4d62-a604-135410d8bdf7">PSM_SETHEADERSUBTITLE</a> message explicitly.


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


#### - pszHeaderSubTitle

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

New header subtitle.


## -remarks



If you specify the current page, it will immediately be repainted to display the new subtitle.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://msdn.microsoft.com/ed4eb370-593f-4893-9de4-1ea9a725b131">PSH_AEROWIZARD</a>).</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a90c1ccc-f25e-476a-bdc5-f4fb568a3cb5">PropSheet_HwndToIndex</a>



<a href="https://msdn.microsoft.com/42baab9e-d713-4f67-87af-d2ea8a586142">PropSheet_IdToIndex</a>



<a href="https://msdn.microsoft.com/e93d4d3f-a046-4f2b-8eab-91bf33c7cd1d">PropSheet_PageToIndex</a>



<b>Reference</b>
 

 

