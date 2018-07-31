---
UID: NF:uiautomationcoreapi.DockPattern_SetDockPosition
title: DockPattern_SetDockPosition function
author: windows-sdk-content
description: Docks the UI Automation element at the requested dockPosition within a docking container.
old-location: winauto\uiauto_DockPattern_SetDockPositionConPat.htm
old-project: WinAuto
ms.assetid: 45fdd85f-1f35-4cdd-adfc-086e01e85adf
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: DockPattern_SetDockPosition, DockPattern_SetDockPosition function [Windows Accessibility], uiauto.uiauto_DockPattern_SetDockPositionConPat, uiauto_DockPattern_SetDockPositionConPat, uiautomationcoreapi/DockPattern_SetDockPosition, winauto.uiauto_DockPattern_SetDockPositionConPat
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - DockPattern_SetDockPosition
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# DockPattern_SetDockPosition function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Docks the UI Automation element at the requested <i>dockPosition</i> within a docking container.


## -parameters




### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The <i>control pattern</i> object.


### -param dockPosition [in]

Type: <b><a href="https://msdn.microsoft.com/36ed98c2-f111-4192-8ce2-b8dd7da47de5">DockPosition</a></b>

The location to dock the control to.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



