---
UID: NF:winddi.EngEraseSurface
title: EngEraseSurface function
author: windows-sdk-content
description: The EngEraseSurface function calls GDI to erase the surface; a given rectangle on the surface will be filled with the given color.
old-location: display\engerasesurface.htm
old-project: display
ms.assetid: 3dace2e1-2a6b-42e5-a556-a3952cf4786c
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: EngEraseSurface, EngEraseSurface function [Display Devices], display.engerasesurface, gdifncs_49673ad2-d8a0-4c8b-bf0f-c1fab9f3c519.xml, winddi/EngEraseSurface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngEraseSurface
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngEraseSurface function


## -description


The <b>EngEraseSurface</b> function calls GDI to erase the surface; a given rectangle on the surface will be filled with the given color.


## -parameters




### -param pso

Pointer to the surface to erase.


### -param prcl

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure that defines which pixels to erase on the surface. This rectangle is exclusive of the bottom and right edges.


### -param iColor [in]

Specifies a color index. This is an index to the value that will be written into each pixel.


## -returns



The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is reported.



