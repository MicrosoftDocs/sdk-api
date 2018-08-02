---
UID: NE:uiribbon.UI_CONTEXTAVAILABILITY
title: UI_CONTEXTAVAILABILITY
author: windows-sdk-content
description: Specifies values that identify the availability of a contextual tab.
old-location: windowsribbon\windowsribbon_ui_contextavailability.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\enums\ui_contextavailability.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: UI_CONTEXTAVAILABILITY, UI_CONTEXTAVAILABILITY enumeration [Windows Ribbon], UI_CONTEXTAVAILABILITY_ACTIVE, UI_CONTEXTAVAILABILITY_AVAILABLE, UI_CONTEXTAVAILABILITY_NOTAVAILABLE, scenicintent_UI_CONTEXTAVAILABILITY, uiribbon/UI_CONTEXTAVAILABILITY, uiribbon/UI_CONTEXTAVAILABILITY_ACTIVE, uiribbon/UI_CONTEXTAVAILABILITY_AVAILABLE, uiribbon/UI_CONTEXTAVAILABILITY_NOTAVAILABLE, windowsribbon.windowsribbon_ui_contextavailability
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UI_CONTEXTAVAILABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uiribbon.h
api_name:
 - UI_CONTEXTAVAILABILITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# UI_CONTEXTAVAILABILITY enumeration


## -description


Specifies values that identify the availability of a <a href="https://msdn.microsoft.com/en-us/library/Dd316798(v=VS.85).aspx">contextual tab</a>.


## -enum-fields




### -field UI_CONTEXTAVAILABILITY_NOTAVAILABLE

A contextual tab is not available for the selected object.


### -field UI_CONTEXTAVAILABILITY_AVAILABLE

A contextual tab is available for the selected object. The tab is not the active tab.


### -field UI_CONTEXTAVAILABILITY_ACTIVE

A contextual tab is available for the selected object. The tab is the active tab.


## -remarks



A contextual tab  is displayed based on the <b>UI_CONTEXTAVAILABILITY</b> value in <a href="https://msdn.microsoft.com/en-us/library/Dd940399(v=VS.85).aspx">UI_PKEY_ContextAvailable</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd371540(v=VS.85).aspx">Constants and Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd940399(v=VS.85).aspx">UI_PKEY_ContextAvailable</a>
 

 

