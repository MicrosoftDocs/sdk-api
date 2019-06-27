---
UID: NS:winuser.__unnamed_struct_1
title: POWERBROADCAST_SETTING (winuser.h)
author: windows-sdk-content
description: Sent with a power setting event and contains data about the specific change.
old-location: base\powerbroadcast_setting.htm
tech.root: power
ms.assetid: 13fa8220-bad2-4bb6-b652-38fc11a31215
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PPOWERBROADCAST_SETTING, POWERBROADCAST_SETTING, POWERBROADCAST_SETTING structure, PPOWERBROADCAST_SETTING, PPOWERBROADCAST_SETTING structure pointer, base.powerbroadcast_setting, winuser/POWERBROADCAST_SETTING, winuser/PPOWERBROADCAST_SETTING"
ms.topic: struct
f1_keywords: 
 - "winuser/POWERBROADCAST_SETTING"
req.header: winuser.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinUser.h
api_name:
 - POWERBROADCAST_SETTING
product: Windows
targetos: Windows
req.typenames: POWERBROADCAST_SETTING, *PPOWERBROADCAST_SETTING
req.redist: 
ms.custom: 19H1
---

# POWERBROADCAST_SETTING structure


## -description


Sent with a power setting event and contains data about the specific change. For more 
    information, see <a href="https://docs.microsoft.com/windows/desktop/Power/registering-for-power-events">Registering for Power 
    Events</a> and <a href="https://docs.microsoft.com/windows/desktop/Power/power-setting-guids">Power Setting GUIDs</a>.


## -struct-fields




### -field PowerSetting

Indicates the power setting for which this notification is being delivered. For more 
    info, see <a href="https://docs.microsoft.com/windows/desktop/Power/power-setting-guids">Power Setting GUIDs</a>.


### -field DataLength

The size in bytes of the data in the  <i>Data</i> member.


### -field Data

The new value of the power setting. The type and possible values for this member depend on <i>PowerSettng.</i>


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Power/power-setting-guids">Power Setting GUIDs</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/registering-for-power-events">Registering for Power Events</a>
 

 

