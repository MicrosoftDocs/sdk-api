---
UID: NF:uxtheme.GetThemeAnimationProperty
title: GetThemeAnimationProperty function
author: windows-sdk-content
description: Gets a theme animation property based on the storyboard id and the target id.
old-location: controls\getthemeanimationproperty.htm
tech.root: controls
ms.assetid: CEFB457B-2022-4FCC-AF1E-78A62D62E034
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetThemeAnimationProperty, GetThemeAnimationProperty function [Windows Controls], controls.getthemeanimationproperty, uxtheme/GetThemeAnimationProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
 - Ext-MS-Win-UXTheme-Themes-l1-1-0.dll
 - xamlpalwp.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
api_name:
 - GetThemeAnimationProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetThemeAnimationProperty function


## -description


Gets a theme animation property based
on the storyboard id and the target id.


## -parameters




### -param hTheme [in]

An opened theme handle.


### -param iStoryboardId [in]

A predefined storyboard identifier.


### -param iTargetId [in]

A predefined target identifier.


### -param eProperty [in]

The property that is associated with the animation storyboard and target.


### -param pvProperty [out]

The buffer to receive the returned property value.


### -param cbSize [in]

The byte size of a buffer that is pointed by <i>pvProperty</i>.


### -param pcbSizeOut [out]

The                                    byte  size of the returned 
property.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



