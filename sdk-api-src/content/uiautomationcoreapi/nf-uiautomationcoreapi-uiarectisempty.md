---
UID: NF:uiautomationcoreapi.UiaRectIsEmpty
title: UiaRectIsEmpty function
author: windows-sdk-content
description: Gets a Boolean value that specifies whether a rectangle has all its coordinates set to 0.
old-location: winauto\uiauto_UiaRectIsEmptyFunction.htm
tech.root: WinAuto
ms.assetid: a1bcf983-a40c-4a9f-95f8-3124d62e07a3
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: UiaRectIsEmpty, UiaRectIsEmpty function [Windows Accessibility], uiauto.uiauto_UiaRectIsEmptyFunction, uiauto_UiaRectIsEmptyFunction, uiautomationcoreapi/UiaRectIsEmpty, winauto.uiauto_UiaRectIsEmptyFunction
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
 - UiaRectIsEmpty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaRectIsEmpty function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Gets a Boolean value that specifies whether a rectangle has all its coordinates set to 0.


## -parameters




### -param rc [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/99cf7e3e-6b36-41ca-ac27-a7b332e7c91e">UiaRect</a></b>

A reference to a <a href="https://msdn.microsoft.com/99cf7e3e-6b36-41ca-ac27-a7b332e7c91e">UiaRect</a> structure that contains the coordinates of the rectangle.


## -returns



Type: <b>bool</b>

<b>TRUE</b> if the rectangle is empty; otherwise <b>FALSE</b>.



