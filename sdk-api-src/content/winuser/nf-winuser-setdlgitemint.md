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

# SetDlgItemInt function


## -description


Sets the text of a control in a dialog box to the string representation of a specified integer value. 


## -parameters




### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box that contains the control. 


### -param nIDDlgItem [in]

Type: <b>int</b>

The control to be changed. 


### -param uValue [in]

Type: <b>UINT</b>

The integer value used to generate the item text. 


### -param bSigned [in]

Type: <b>BOOL</b>

Indicates whether the <i>uValue</i> parameter is signed or unsigned. If this parameter is <b>TRUE</b>, <i>uValue</i> is signed. If this parameter is <b>TRUE</b> and <i>uValue</i> is less than zero, a minus sign is placed before the first digit in the string. If this parameter is <b>FALSE</b>, <i>uValue</i> is unsigned. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



To set the new text, this function sends a <a href="https://msdn.microsoft.com/1b48c309-6903-4139-bf42-e8526963e681">WM_SETTEXT</a> message to the specified control.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/8a0b8275-35e5-4983-9b2d-968023d39aa3">GetDlgItemInt</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/af359c1c-f3ec-4901-97bb-3fb654f44598">SetDlgItemText</a>



<a href="https://msdn.microsoft.com/1b48c309-6903-4139-bf42-e8526963e681">WM_SETTEXT</a>
 

 

