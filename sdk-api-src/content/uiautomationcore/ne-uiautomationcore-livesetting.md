---
UID: NE:uiautomationcore.LiveSetting
title: LiveSetting (uiautomationcore.h)
description: Contains possible values for the LiveSetting property. This property is implemented by provider elements that are part of a live region.
helpviewer_keywords: ["LiveSetting","LiveSetting enumeration [Windows Accessibility]","LiveSetting_Assertive","LiveSetting_Off","LiveSetting_Polite","uiautomationcore/LiveSetting","uiautomationcore/LiveSetting_Assertive","uiautomationcore/LiveSetting_Off","uiautomationcore/LiveSetting_Polite","winauto.uiauto_LiveSetting"]
old-location: winauto\uiauto_LiveSetting.htm
tech.root: WinAuto
ms.assetid: 40DD1F00-A9BC-4C84-B2A3-940E37EE9C19
ms.date: 12/05/2018
ms.keywords: LiveSetting, LiveSetting enumeration [Windows Accessibility], LiveSetting_Assertive, LiveSetting_Off, LiveSetting_Polite, uiautomationcore/LiveSetting, uiautomationcore/LiveSetting_Assertive, uiautomationcore/LiveSetting_Off, uiautomationcore/LiveSetting_Polite, winauto.uiauto_LiveSetting
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - LiveSetting
 - uiautomationcore/LiveSetting
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
 - LiveSetting
---

# LiveSetting enumeration


## -description

Contains possible values for the LiveSetting property. This property is implemented by provider elements that are part of a live region.

## -enum-fields

### -field Off:0

### -field Polite:1

### -field Assertive:2

#### - LiveSetting_Assertive

The provider element sends change notifications when the content of the live region changes, and a client should immediately notify the user of each change.


#### - LiveSetting_Off

The provider element does not send change notifications when the content of the live region changes. A client application will be aware of changes to the live region only if the client handles other events related to the elements in the live region.


#### - LiveSetting_Polite

The provider element sends change notifications when the content of the live region changes, but a client should not interrupt the user to inform the user of changes. Instead, the client should wait until the user is not performing high-priority actions and wants to receive low-priority notifications.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement2-get_cachedlivesetting">CachedLiveSetting</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement2-get_currentlivesetting">CurrentLiveSetting</a>
