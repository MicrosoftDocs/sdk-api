---
UID: NF:uiautomationcoreapi.TransformPattern_Move
title: TransformPattern_Move function
author: windows-sdk-content
description: Moves an element to a specified location on the screen.
old-location: winauto\uiauto_TransformPattern_MoveConPat.htm
tech.root: WinAuto
ms.assetid: 283bf97f-b5fd-438c-b923-9aca97a69e1b
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: TransformPattern_Move, TransformPattern_Move function [Windows Accessibility], uiauto.uiauto_TransformPattern_MoveConPat, uiauto_TransformPattern_MoveConPat, uiautomationcoreapi/TransformPattern_Move, winauto.uiauto_TransformPattern_MoveConPat
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - TransformPattern_Move
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TransformPattern_Move function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Moves an element to a specified location on the screen.


## -parameters




### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.


### -param x [in]

Type: <b>double</b>

The horizontal screen coordinate to move the element to.


### -param y [in]

Type: <b>double</b>

The vertical screen coordinate to move the element to.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



