---
UID: NS:winuser.POWERBROADCAST_SETTING
title: POWERBROADCAST_SETTING
author: windows-sdk-content
description: Sent with a power setting event and contains data about the specific change.
old-location: base\powerbroadcast_setting.htm
tech.root: power
ms.assetid: 13fa8220-bad2-4bb6-b652-38fc11a31215
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: "*PPOWERBROADCAST_SETTING, POWERBROADCAST_SETTING, POWERBROADCAST_SETTING structure, PPOWERBROADCAST_SETTING, PPOWERBROADCAST_SETTING structure pointer, base.powerbroadcast_setting, winuser/POWERBROADCAST_SETTING, winuser/PPOWERBROADCAST_SETTING"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
---

# POWERBROADCAST_SETTING structure


## -description


Sent with a power setting event and contains data about the specific change. For more 
    information, see <a href="https://msdn.microsoft.com/840390ca-d32a-4cf3-9e75-66322c7cdee0">Registering for Power 
    Events</a> and <a href="https://msdn.microsoft.com/39D432A7-54F8-4135-B98C-7290F95B054A">Power Setting GUIDs</a>.


## -struct-fields




### -field PowerSetting

Indicates the power setting for which this notification is being delivered. For more 
    info, see <a href="https://msdn.microsoft.com/39D432A7-54F8-4135-B98C-7290F95B054A">Power Setting GUIDs</a>.


### -field DataLength

The size in bytes of the data in the  <i>Data</i> member.


### -field Data

The new value of the power setting. The type and possible values for this member depend on <i>PowerSettng.</i>


## -see-also




<a href="https://msdn.microsoft.com/39D432A7-54F8-4135-B98C-7290F95B054A">Power Setting GUIDs</a>



<a href="https://msdn.microsoft.com/840390ca-d32a-4cf3-9e75-66322c7cdee0">Registering for Power Events</a>
 

 

