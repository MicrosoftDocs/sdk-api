---
UID: NS:winuser.POWERBROADCAST_SETTING
title: POWERBROADCAST_SETTING (winuser.h)
description: Sent with a power setting event and contains data about the specific change.
helpviewer_keywords: ["*PPOWERBROADCAST_SETTING","POWERBROADCAST_SETTING","POWERBROADCAST_SETTING structure","PPOWERBROADCAST_SETTING","PPOWERBROADCAST_SETTING structure pointer","base.powerbroadcast_setting","winuser/POWERBROADCAST_SETTING","winuser/PPOWERBROADCAST_SETTING"]
old-location: base\powerbroadcast_setting.htm
tech.root: base
ms.assetid: 13fa8220-bad2-4bb6-b652-38fc11a31215
ms.date: 12/05/2018
ms.keywords: '*PPOWERBROADCAST_SETTING, POWERBROADCAST_SETTING, POWERBROADCAST_SETTING structure, PPOWERBROADCAST_SETTING, PPOWERBROADCAST_SETTING structure pointer, base.powerbroadcast_setting, winuser/POWERBROADCAST_SETTING, winuser/PPOWERBROADCAST_SETTING'
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
targetos: Windows
req.typenames: POWERBROADCAST_SETTING, *PPOWERBROADCAST_SETTING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PPOWERBROADCAST_SETTING
 - winuser/PPOWERBROADCAST_SETTING
 - POWERBROADCAST_SETTING
 - winuser/POWERBROADCAST_SETTING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinUser.h
api_name:
 - POWERBROADCAST_SETTING
---

# POWERBROADCAST_SETTING structure


## -description

Sent with a power setting event and contains data about the specific change. For more 
    information, see <a href="/windows/desktop/Power/registering-for-power-events">Registering for Power 
    Events</a> and <a href="/windows/desktop/Power/power-setting-guids">Power Setting GUIDs</a>.

## -struct-fields

### -field PowerSetting

Indicates the power setting for which this notification is being delivered. For more 
    info, see <a href="/windows/desktop/Power/power-setting-guids">Power Setting GUIDs</a>.

### -field DataLength

The size in bytes of the data in the  <i>Data</i> member.

### -field Data

The new value of the power setting. The type and possible values for this member depend on <i>PowerSettng.</i>

## -see-also

<a href="/windows/desktop/Power/power-setting-guids">Power Setting GUIDs</a>



<a href="/windows/desktop/Power/registering-for-power-events">Registering for Power Events</a>

