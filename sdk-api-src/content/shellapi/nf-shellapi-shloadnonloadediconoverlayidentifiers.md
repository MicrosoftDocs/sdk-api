---
UID: NF:shellapi.SHLoadNonloadedIconOverlayIdentifiers
title: SHLoadNonloadedIconOverlayIdentifiers function
author: windows-sdk-content
description: Signals the Shell that during the next operation requiring overlay information, it should load icon overlay identifiers that either failed creation or were not present for creation at startup. Identifiers that have already been loaded are not affected.
old-location: shell\SHLoadNonloadedIconOverlayIdentifiers.htm
old-project: shell
ms.assetid: d2c4f37e-6e9d-4536-90ea-d69461c4105a
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SHLoadNonloadedIconOverlayIdentifiers, SHLoadNonloadedIconOverlayIdentifiers function [Windows Shell], _shell_shloadnonloadediconoverlayidentifiers, shell.SHLoadNonloadedIconOverlayIdentifiers, shellapi/SHLoadNonloadedIconOverlayIdentifiers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shellapi.h
req.include-header: 
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
req.typenames: SHSTOCKICONID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
api_name:
-	SHLoadNonloadedIconOverlayIdentifiers
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHLoadNonloadedIconOverlayIdentifiers function


## -description


Signals the Shell that during the next operation requiring overlay information, it should load icon overlay identifiers that either failed creation or were not present for creation at startup. Identifiers that have already been loaded are not affected.


## -parameters






## -returns



Type: <b>HRESULT</b>

Always returns S_OK.




## -remarks



A call to <b>SHLoadNonloadedIconOverlayIdentifiers</b> does not result in the immediate loading of a Shell extension, nor does it cause an icon overlay handler to be loaded. A call to <b>SHLoadNonloadedIconOverlayIdentifiers</b> results in a situation such that the next code to ask for icon overlay information triggers a comparison of icon overlays in the registry to those that are already loaded. If an icon overlay is newly registered and the system has not already reached its upper limit of fifteen icon overlays, the new overlay is loaded. <b>SHLoadNonloadedIconOverlayIdentifiers</b> alone does not load a new icon overlay; you also need to trigger an action that uses the overlay, such as a refresh of a Windows Explorer view.

For more information, see <a href="https://msdn.microsoft.com/ADF27BFD-CC96-43F9-9EBB-DEBE0DEA7B92">How to Implement Icon Overlay Handlers</a>.



