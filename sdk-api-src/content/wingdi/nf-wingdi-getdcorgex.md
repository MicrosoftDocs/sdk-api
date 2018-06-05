---
UID: NF:wingdi.GetDCOrgEx
title: GetDCOrgEx function
author: windows-sdk-content
description: The GetDCOrgEx function retrieves the final translation origin for a specified device context (DC).
old-location: gdi\getdcorgex.htm
old-project: gdi
ms.assetid: 795c6a69-7146-4d1a-abf9-ce1d740ca946
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetDCOrgEx, GetDCOrgEx function [Windows GDI], _win32_GetDCOrgEx, gdi.getdcorgex, wingdi/GetDCOrgEx
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-DC-l1-2-0.dll
-	ext-ms-win-gdi-dc-l1-1-0.dll
-	ext-ms-win-gdi-dc-l1-2-1.dll
-	GDI32Full.dll
api_name:
-	GetDCOrgEx
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetDCOrgEx function


## -description


The <b>GetDCOrgEx</b> function retrieves the final translation origin for a specified device context (DC). The final translation origin specifies an offset that the system uses to translate device coordinates into client coordinates (for coordinates in an application's window).


## -parameters




### -param hdc [in]

A handle to the DC whose final translation origin is to be retrieved.


### -param lppt

TBD




#### - lpPoint [out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that receives the final translation origin, in device coordinates.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The final translation origin is relative to the physical origin of the screen.




## -see-also




<a href="https://msdn.microsoft.com/dcb08ce7-9ded-497c-936c-48d3026a0004">CreateIC</a>



<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>
 

 

