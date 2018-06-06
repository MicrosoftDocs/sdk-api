---
UID: NS:uxtheme._WTA_OPTIONS
title: "_WTA_OPTIONS"
author: windows-sdk-content
description: Defines options that are used to set window visual style attributes.
old-location: controls\WTA_OPTIONS.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\structures\wta_options.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: "*PWTA_OPTIONS, PWTA_OPTIONS, PWTA_OPTIONS structure pointer [Windows Controls], WTA_OPTIONS, WTA_OPTIONS structure [Windows Controls], _WTA_OPTIONS, controls.WTA_OPTIONS, controls.inet_WTA_OPTIONS, inet_WTA_OPTIONS, inet_WTA_OPTIONS_cpp, uxtheme/PWTA_OPTIONS, uxtheme/WTA_OPTIONS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: WTA_OPTIONS, *PWTA_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uxtheme.h
api_name:
 - WTA_OPTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _WTA_OPTIONS structure


## -description


Defines options that are used to set window visual style attributes.


## -struct-fields




### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A combination of flags that modify window visual style attributes. Can be a combination of the <a href="https://msdn.microsoft.com/C71D1957-6572-4242-B715-C54BDFBBD6B7">WTNCA</a> constants.


### -field dwMask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A bitmask that describes how the values specified in <b>dwFlags</b> should be applied. If the bit corresponding to a value in <b>dwFlags</b> is 0, that flag will be removed. If the bit is 1, the flag will be added.


## -see-also




<a href="https://msdn.microsoft.com/be757193-4f77-456f-bdf5-1e873bf1fac4">SetWindowThemeAttribute</a>
 

 

