---
UID: NF:expandedresources.GetExpandedResourceExclusiveCpuCount
title: GetExpandedResourceExclusiveCpuCount function
author: windows-sdk-content
description: Gets the expected number of exclusive CPU sets that are available to the app when in Game Mode.
old-location: gamemode\getexpandedresourceexclusivecpucount.htm
old-project: gamemode
ms.assetid: C87BE7FE-9CC7-4B6B-AC25-606A967D70C6
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetExpandedResourceExclusiveCpuCount, GetExpandedResourceExclusiveCpuCount function, expandedresources/GetExpandedResourceExclusiveCpuCount, gamemode.getexpandedresourceexclusivecpucount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: ShellWindowTypeConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gamemode.dll
api_name:
 - GetExpandedResourceExclusiveCpuCount
product: Windows
targetos: Windows
req.lib: Windowsapp.lib
req.dll: Gamemode.dll
req.irql: 
req.product: Internet Explorer 5
---

# GetExpandedResourceExclusiveCpuCount function


## -description


Gets the expected number of exclusive CPU sets that are available to the app when in Game Mode.


## -parameters




### -param exclusiveCpuCount [out]

The expected number of exclusive CPU sets that are available to the app when in Game Mode.


## -returns



The result of the operation.




## -remarks



This is a Win32 API that's supported in UWP desktop and Xbox apps, as well as Win32 apps.

You can use this function to determine what resources are available to your app, and use this information to decide whether to enter Game Mode or shared mode.

This function returns 0 if no exclusive CPU sets are available, or if the customer opted out of Game Mode via the Settings in Windows 10.

The app must be in the foreground and have focus before exclusive resources are granted.



