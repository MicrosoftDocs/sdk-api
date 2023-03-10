---
UID: NF:uiautomationcoreapi.DockPattern_SetDockPosition
title: DockPattern_SetDockPosition function (uiautomationcoreapi.h)
description: Docks the UI Automation element at the requested dockPosition within a docking container.
helpviewer_keywords: ["DockPattern_SetDockPosition","DockPattern_SetDockPosition function [Windows Accessibility]","uiauto.uiauto_DockPattern_SetDockPositionConPat","uiauto_DockPattern_SetDockPositionConPat","uiautomationcoreapi/DockPattern_SetDockPosition","winauto.uiauto_DockPattern_SetDockPositionConPat"]
old-location: winauto\uiauto_DockPattern_SetDockPositionConPat.htm
tech.root: WinAuto
ms.assetid: 45fdd85f-1f35-4cdd-adfc-086e01e85adf
ms.date: 12/05/2018
ms.keywords: DockPattern_SetDockPosition, DockPattern_SetDockPosition function [Windows Accessibility], uiauto.uiauto_DockPattern_SetDockPositionConPat, uiauto_DockPattern_SetDockPositionConPat, uiautomationcoreapi/DockPattern_SetDockPosition, winauto.uiauto_DockPattern_SetDockPositionConPat
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DockPattern_SetDockPosition
 - uiautomationcoreapi/DockPattern_SetDockPosition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - DockPattern_SetDockPosition
---

# DockPattern_SetDockPosition function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Docks the UI Automation element at the requested <i>dockPosition</i> within a docking container.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The <i>control pattern</i> object.

### -param dockPosition [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-dockposition">DockPosition</a></b>

The location to dock the control to.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.