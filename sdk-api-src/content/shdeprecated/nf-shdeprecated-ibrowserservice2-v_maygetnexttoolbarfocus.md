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

# IBrowserService2::v_MayGetNextToolbarFocus


## -description


Deprecated. Used when translating accelerators through <a href="https://msdn.microsoft.com/dda5c085-7199-4b83-b03e-e4c715665157">TranslateAcceleratorSB</a> and in checking the cycle of focus between the view and the browser's toolbars.


## -parameters




### -param lpMsg [in]

Type: <b>LPMSG</b>

A pointer to a <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a> that contains the keystroke message.


### -param itbNext [in]

Type: <b>UINT</b>

The index of the next toolbar, or ITB_VIEW if focus is shifting to the view.


### -param citb [in]

Type: <b>int</b>

The ID of the current toolbar with focus, or ITB_VIEW if the view has focus.


### -param pptbi [out]

Type: <b>LPTOOLBARITEM*</b>

A pointer to a <a href="https://msdn.microsoft.com/7378f2f3-c164-46fe-9989-a7a57fceb48a">TOOLBARITEM</a> structure that represents the toolbar receiving the focus.


### -param phwnd [out]

Type: <b>HWND*</b>

A pointer to the handle of the window that contains the toolbar.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



