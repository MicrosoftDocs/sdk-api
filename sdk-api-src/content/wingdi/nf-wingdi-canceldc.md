---
UID: NF:wingdi.CancelDC
title: CancelDC function
author: windows-driver-content
description: The CancelDC function cancels any pending operation on the specified device context (DC).
old-location: gdi\canceldc.htm
old-project: gdi
ms.assetid: 1dcb3dfe-0ab0-4bf5-ac2f-7a9c11712eef
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: CancelDC, CancelDC function [Windows GDI], _win32_CancelDC, gdi.canceldc, wingdi/CancelDC
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
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
req.typenames: FAX_TIME, *PFAX_TIME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	CancelDC
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CancelDC function


## -description


The <b>CancelDC</b> function cancels any pending operation on the specified device context (DC).


## -parameters




### -param hdc [in]

A handle to the DC.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>CancelDC</b> function is used by multithreaded applications to cancel lengthy drawing operations. If thread A initiates a lengthy drawing operation, thread B may cancel that operation by calling this function.

If an operation is canceled, the affected thread returns an error and the result of its drawing operation is undefined. The results are also undefined if no drawing operation was in progress when the function was called.




## -see-also




<a href="https://msdn.microsoft.com/202a4b42-513a-45de-894a-72e56c706a58">CreateThread</a>



<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/91a11552-66c1-42bd-b837-8a7685977bc9">GetCurrentThread</a>
 

 

