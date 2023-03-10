---
UID: NS:uiautomationcore.UIAutomationEventInfo
title: UIAutomationEventInfo (uiautomationcore.h)
description: Contains information about a custom event.
helpviewer_keywords: ["UIAutomationEventInfo","UIAutomationEventInfo structure [Windows Accessibility]","uiauto.uiauto_UIAutomationEventInfoStruct","uiauto_UIAutomationEventInfoStruct","uiautomationcore/UIAutomationEventInfo","winauto.uiauto_UIAutomationEventInfoStruct"]
old-location: winauto\uiauto_UIAutomationEventInfoStruct.htm
tech.root: WinAuto
ms.assetid: 05dd033f-3bb2-4185-9cfc-c19927a82406
ms.date: 12/05/2018
ms.keywords: UIAutomationEventInfo, UIAutomationEventInfo structure [Windows Accessibility], uiauto.uiauto_UIAutomationEventInfoStruct, uiauto_UIAutomationEventInfoStruct, uiautomationcore/UIAutomationEventInfo, winauto.uiauto_UIAutomationEventInfoStruct
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UIAutomationEventInfo
 - uiautomationcore/UIAutomationEventInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationCore.h
api_name:
 - UIAutomationEventInfo
---

# UIAutomationEventInfo structure


## -description

Contains information about a custom event.

## -struct-fields

### -field guid

Type: <b>GUID</b>

The event identifier.

### -field pProgrammaticName

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The programmatic name of the event (a non-localizable string).

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-custompropertieseventscontrolpatterns">Custom Properties, Events, and Control Patterns</a>



<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iuiautomationregistrar-registerevent">RegisterEvent</a>