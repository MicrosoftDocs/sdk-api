---
UID: NE:uiribbon.UI_CONTEXTAVAILABILITY
title: UI_CONTEXTAVAILABILITY (uiribbon.h)
author: windows-sdk-content
description: Specifies values that identify the availability of a contextual tab.
old-location: windowsribbon\windowsribbon_ui_contextavailability.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\enums\ui_contextavailability.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: UI_CONTEXTAVAILABILITY, UI_CONTEXTAVAILABILITY enumeration [Windows Ribbon], UI_CONTEXTAVAILABILITY_ACTIVE, UI_CONTEXTAVAILABILITY_AVAILABLE, UI_CONTEXTAVAILABILITY_NOTAVAILABLE, scenicintent_UI_CONTEXTAVAILABILITY, uiribbon/UI_CONTEXTAVAILABILITY, uiribbon/UI_CONTEXTAVAILABILITY_ACTIVE, uiribbon/UI_CONTEXTAVAILABILITY_AVAILABLE, uiribbon/UI_CONTEXTAVAILABILITY_NOTAVAILABLE, windowsribbon.windowsribbon_ui_contextavailability
ms.topic: enum
f1_keywords: 
 - "uiribbon/UI_CONTEXTAVAILABILITY"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: UI_CONTEXTAVAILABILITY
req.redist: 
ms.custom: 19H1
---

# UI_CONTEXTAVAILABILITY enumeration


## -description


Specifies values that identify the availability of a <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-element-ribbon-contextualtabs">contextual tab</a>.


## -enum-fields




### -field UI_CONTEXTAVAILABILITY_NOTAVAILABLE

A contextual tab is not available for the selected object.


### -field UI_CONTEXTAVAILABILITY_AVAILABLE

A contextual tab is available for the selected object. The tab is not the active tab.


### -field UI_CONTEXTAVAILABILITY_ACTIVE

A contextual tab is available for the selected object. The tab is the active tab.


## -remarks



A contextual tab  is displayed based on the <b>UI_CONTEXTAVAILABILITY</b> value in <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-contextavailable">UI_PKEY_ContextAvailable</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-reference-enumerations">Constants and Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-contextavailable">UI_PKEY_ContextAvailable</a>
 

 

