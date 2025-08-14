---
UID: NF:expandedresources.HasExpandedResources
title: HasExpandedResources function (expandedresources.h)
description: Gets the current resource state (that is, whether the app is running in Game Mode or shared mode).
helpviewer_keywords: ["HasExpandedResources","HasExpandedResources function","expandedresources/HasExpandedResources","gamemode.hasexpandedresources"]
old-location: gamemode\hasexpandedresources.htm
tech.root: gamemode
ms.assetid: E0434DBD-4C1A-4675-94A3-4954BCC67CD5
ms.date: 12/05/2018
ms.keywords: HasExpandedResources, HasExpandedResources function, expandedresources/HasExpandedResources, gamemode.hasexpandedresources
req.header: expandedresources.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: Windowsapp.lib
req.dll: Gamemode.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HasExpandedResources
 - expandedresources/HasExpandedResources
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-gaming-expandedresources-l1-1-0.dll
 - gamemode.dll
api_name:
 - HasExpandedResources
---

# HasExpandedResources function


## -description

Gets the current resource state (that is, whether the app is running in Game Mode or shared mode).

## -parameters

### -param hasExpandedResources [out]

True if  the app is running in Game Mode; otherwise, false.

## -returns

The result of the operation.

## -remarks

This is a Win32 API that's supported in UWP desktop and Xbox apps, as well as Win32 apps.

This function should be called during each iteration of the game loop to check when the app enters and exits Game Mode so that the appropriate settings can be applied.

The app must be in the foreground and have focus before exclusive resources are granted.

