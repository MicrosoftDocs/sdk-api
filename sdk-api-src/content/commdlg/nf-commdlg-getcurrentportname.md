---
UID: NF:commdlg.GetCurrentPortName
title: GetCurrentPortName function
author: windows-driver-content
description: Retrieves the name of the current port for use with PrintDlgEx.
old-location: dlgbox\iprintdialogservices_getcurrentportname.htm
old-project: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxinterfaces\iprintdialogservices\iprintdialogservicesgetcurrentportname.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: GetCurrentPortName, GetCurrentPortName function, GetCurrentPortName method [Dialog Boxes], GetCurrentPortName method [Dialog Boxes],IPrintDialogServices interface, IPrintDialogServices interface [Dialog Boxes],GetCurrentPortName method, IPrintDialogServices::GetCurrentPortName, _win32_IPrintDialogServices_GetCurrentPortName, _win32_iprintdialogservices_getcurrentportname_cpp, commdlg/IPrintDialogServices::GetCurrentPortName, dlgbox.iprintdialogservices_getcurrentportname, winui._win32_iprintdialogservices_getcurrentportname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UDACCEL, *LPUDACCEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Comdlg32.dll
api_name:
-	IPrintDialogServices.GetCurrentPortName
product: Windows
targetos: Windows
req.lib: 
req.dll: Comdlg32.dll
req.irql: 
---

# GetCurrentPortName function


## -description


Retrieves the name of the current port for use with <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a>.


## -parameters




### -param pPortName

TBD


### -param pcchSize

Type: <b>UINT*</b>

On input, the variable specifies the size, in characters, of the buffer pointed to by the <i>lpPortName</i> parameter. On output, the variable contains the number of bytes (ANSI) or characters (Unicode), including the terminating null character, written to the buffer.

If the size is zero on input, the function returns the required buffer size (in bytes or characters) in <i>pcchSize</i> and does not use the <i>lpPortName</i> buffer.


#### - lpPortName

Type: <b>LPTSTR</b>

The name of the current port.


## -returns



Type: <b>HRESULT</b>

If the method is successful, the return value is <b>S_OK</b>. If there is no current port, the return value is <b>S_OK</b>, the value returned in <i>pcchSize</i> is zero, and the <i>lpPortName</i> buffer is unchanged.

If an error occurs, the return value is a COM error code. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>.




## -see-also




<a href="https://msdn.microsoft.com/28573019-f0bd-4a8e-a1a1-48559f658a81">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f8572f39-bccd-40ed-b556-3cac19920f15">IPrintDialogServices</a>



<a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a>



<b>Reference</b>
 

 

