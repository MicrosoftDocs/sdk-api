---
UID: NF:uiautomationcoreapi.TransformPattern_Resize
title: TransformPattern_Resize function (uiautomationcoreapi.h)
author: windows-sdk-content
description: Resizes an element on the screen.
old-location: winauto\uiauto_TransformPattern_ResizeConPat.htm
tech.root: WinAuto
ms.assetid: 114dfef2-7342-4ee2-89ef-7f583c568376
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TransformPattern_Resize, TransformPattern_Resize function [Windows Accessibility], uiauto.uiauto_TransformPattern_ResizeConPat, uiauto_TransformPattern_ResizeConPat, uiautomationcoreapi/TransformPattern_Resize, winauto.uiauto_TransformPattern_ResizeConPat
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - TransformPattern_Resize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TransformPattern_Resize function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Resizes an element on the screen.


## -parameters




### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.


### -param width [in]

Type: <b>double</b>

The width, in pixels, to resize the element to.


### -param height [in]

Type: <b>double</b>

The height, in pixels, to resize the element to.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



