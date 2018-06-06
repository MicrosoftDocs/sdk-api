---
UID: NF:wingdi.CreatePenIndirect
title: CreatePenIndirect function
author: windows-sdk-content
description: The CreatePenIndirect function creates a logical cosmetic pen that has the style, width, and color specified in a structure.
old-location: gdi\createpenindirect.htm
old-project: gdi
ms.assetid: 638c0294-9a8f-44ed-a791-1be152cd92dd
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CreatePenIndirect, CreatePenIndirect function [Windows GDI], _win32_CreatePenIndirect, gdi.createpenindirect, wingdi/CreatePenIndirect
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CreatePenIndirect
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreatePenIndirect function


## -description


The <b>CreatePenIndirect</b> function creates a logical cosmetic pen that has the style, width, and color specified in a structure.


## -parameters




### -param plpen

TBD




#### - lplgpn [in]

Pointer to a <a href="https://msdn.microsoft.com/0e098b5a-e249-43ad-a6d8-2509b6562453">LOGPEN</a> structure that specifies the pen's style, width, and color.


## -returns



If the function succeeds, the return value is a handle that identifies a logical cosmetic pen.

If the function fails, the return value is <b>NULL</b>.




## -remarks



After an application creates a logical pen, it can select that pen into a device context by calling the <a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a> function. After a pen is selected into a device context, it can be used to draw lines and curves.

When you no longer need the pen, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.




## -see-also




<a href="https://msdn.microsoft.com/882facd2-7e06-48f6-82e4-f20e4d5adc92">CreatePen</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a>



<a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a>



<a href="https://msdn.microsoft.com/0e098b5a-e249-43ad-a6d8-2509b6562453">LOGPEN</a>



<a href="https://msdn.microsoft.com/d5cc81b5-0df4-4ec2-8941-d63819a8d5ff">Pen Functions</a>



<a href="https://msdn.microsoft.com/624c3ea6-6e42-4577-9228-961501633937">Pens Overview</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>
 

 

