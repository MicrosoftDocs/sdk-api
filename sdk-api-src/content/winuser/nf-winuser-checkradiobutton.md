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

# CheckRadioButton function


## -description


Adds a check mark to (checks) a specified radio button in a group and removes a check mark from (clears) all other radio buttons in the group. 


## -parameters




### -param hDlg [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the dialog box that contains the radio button. 


### -param nIDFirstButton [in]

Type: <b>int</b>

The identifier of the first radio button in the group. 


### -param nIDLastButton [in]

Type: <b>int</b>

The identifier of the last radio button in the group. 


### -param nIDCheckButton [in]

Type: <b>int</b>

The identifier of the radio button to select. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <b>CheckRadioButton</b> function sends a <a href="https://msdn.microsoft.com/8294e6c4-caac-4c60-85ff-38698a1d2ae4">BM_SETCHECK</a> message to each of the radio buttons in the indicated group.

The <i>nIDFirstButton</i> and <i>nIDLastButton</i> parameters specify a range of button identifiers (normally the resource IDs of the buttons).  The position of buttons in the tab order is irrelevant; if a button forms part of a group, but has an ID outside the specified range, it is not affected by this call.




## -see-also




<a href="https://msdn.microsoft.com/bda42841-cc26-44c7-9295-3b3bc818d269">CheckDlgButton</a>



<a href="https://msdn.microsoft.com/859ff84e-a6d8-466b-9b85-f844a47febdf">IsDlgButtonChecked</a>



<b>Reference</b>
 

 

