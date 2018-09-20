---
UID: NF:uiautomationcoreapi.MultipleViewPattern_SetCurrentView
title: MultipleViewPattern_SetCurrentView function
author: windows-sdk-content
description: Sets a control to a different layout.
old-location: winauto\uiauto_MultipleViewPattern_SetCurrentViewConPat.htm
tech.root: WinAuto
ms.assetid: 346b6099-ca8f-4237-9eda-1ae2ee2263a3
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: MultipleViewPattern_SetCurrentView, MultipleViewPattern_SetCurrentView function [Windows Accessibility], uiauto.uiauto_MultipleViewPattern_SetCurrentViewConPat, uiauto_MultipleViewPattern_SetCurrentViewConPat, uiautomationcoreapi/MultipleViewPattern_SetCurrentView, winauto.uiauto_MultipleViewPattern_SetCurrentViewConPat
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
 - MultipleViewPattern_SetCurrentView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MultipleViewPattern_SetCurrentView function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Sets a control to a different layout.


## -parameters




### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.


### -param viewId [in]

Type: <b>int</b>

The control-specific identifier for the view.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



