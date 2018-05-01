---
UID: NF:wingdi.DeleteDC
title: DeleteDC function
author: windows-driver-content
description: The DeleteDC function deletes the specified device context (DC).
old-location: gdi\deletedc.htm
old-project: gdi
ms.assetid: 1aa549a0-c95f-4385-a30e-8906f67e39cd
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: DeleteDC, DeleteDC function [Windows GDI], _win32_DeleteDC, gdi.deletedc, wingdi/DeleteDC
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-DC-Create-l1-1-0.dll
-	Ext-MS-Win-GDI-DC-Create-l1-1-1.dll
-	ext-ms-win-gdi-dc-create-l1-1-2.dll
-	GDI32Full.dll
api_name:
-	DeleteDC
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DeleteDC function


## -description


The <b>DeleteDC</b> function deletes the specified device context (DC).


## -parameters




### -param hdc [in]

A handle to the device context.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



An application must not delete a DC whose handle was obtained by calling the <a href="https://msdn.microsoft.com/50b2387b-c8e4-42a8-8f0f-0bdb355adbfd">GetDC</a> function. Instead, it must call the <a href="https://msdn.microsoft.com/c4f48f1e-4a37-4330-908e-2ac5c65e1a1d">ReleaseDC</a> function to free the DC.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/7989d393-7be4-47fc-af8d-26dd549c48be">Retrieving the Capabilities of a Printer</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/6fc443c8-da97-4196-a9ed-179a4e583849">CreateDC</a>



<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/50b2387b-c8e4-42a8-8f0f-0bdb355adbfd">GetDC</a>



<a href="https://msdn.microsoft.com/c4f48f1e-4a37-4330-908e-2ac5c65e1a1d">ReleaseDC</a>
 

 

