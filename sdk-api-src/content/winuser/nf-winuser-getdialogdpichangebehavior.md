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

# GetDialogDpiChangeBehavior function


## -description


Returns the flags that might have been set on a given dialog by an earlier call to <a href="https://msdn.microsoft.com/48A13F57-9D82-4F79-962B-FBD02FFF9B39">SetDialogDpiChangeBehavior</a>.

 If that function was never called on the dialog, the return value will be zero.


## -parameters




### -param hDlg

The handle for the dialog to examine.


## -returns



The flags set on the given dialog. If passed an invalid handle, this function will return zero, and set its <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">last error</a> to <b>ERROR_INVALID_HANDLE</b>.




## -remarks



It can be difficult to distinguish between a return value of <b>DDC_DEFAULT</b> and the error case, which is zero. To determine between the two, it is recommended that you call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError()</a> to check the error.




## -see-also




<a href="https://msdn.microsoft.com/26248777-E95F-49BE-82D6-7237FAEE0627">DIALOG_DPI_CHANGE_BEHAVIORS</a>



<a href="https://msdn.microsoft.com/48A13F57-9D82-4F79-962B-FBD02FFF9B39">SetDialogDpiChangeBehavior</a>
 

 

