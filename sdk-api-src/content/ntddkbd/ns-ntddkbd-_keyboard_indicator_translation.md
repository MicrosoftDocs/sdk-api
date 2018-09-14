---
UID: NS:ntddkbd._KEYBOARD_INDICATOR_TRANSLATION
title: "_KEYBOARD_INDICATOR_TRANSLATION"
author: windows-sdk-content
description: KEYBOARD_INDICATOR_TRANSLATION specifies a device-specific, variable length array of mappings between keyboard scan codes and LED indicators.
old-location: hid\keyboard_indicator_translation.htm
tech.root: hid
ms.assetid: 7ee6ab87-b8fa-4d2c-a51f-5a20ed836d6a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PKEYBOARD_INDICATOR_TRANSLATION, KEYBOARD_INDICATOR_TRANSLATION, KEYBOARD_INDICATOR_TRANSLATION structure [Human Input Devices], PKEYBOARD_INDICATOR_TRANSLATION, PKEYBOARD_INDICATOR_TRANSLATION structure pointer [Human Input Devices], _KEYBOARD_INDICATOR_TRANSLATION, hid.keyboard_indicator_translation, kref_937bedf9-89bf-4db8-ad4d-2e8354a163f6.xml, ntddkbd/KEYBOARD_INDICATOR_TRANSLATION, ntddkbd/PKEYBOARD_INDICATOR_TRANSLATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntddkbd.h
req.include-header: Ntddkbd.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddkbd.h
api_name:
 - KEYBOARD_INDICATOR_TRANSLATION
product: Windows
targetos: Windows
req.typenames: KEYBOARD_INDICATOR_TRANSLATION, *PKEYBOARD_INDICATOR_TRANSLATION
req.redist: 
---

# _KEYBOARD_INDICATOR_TRANSLATION structure


## -description


KEYBOARD_INDICATOR_TRANSLATION specifies a device-specific, variable length array of mappings between keyboard scan codes and LED indicators.


## -struct-fields




### -field NumberOfIndicatorKeys

Specifies the number of elements in the <b>IndicatorList</b> array.


### -field IndicatorList

Specifies a device-specific, variable-length array of INDICATOR_LIST structures.


```
typedef struct _INDICATOR_LIST {
  USHORT  MakeCode;
  USHORT  IndicatorFlags;
} INDICATOR_LIST, *PINDICATOR_LIST;
```






#### MakeCode

Specifies the make scan code that is generated when a key is pressed.



#### IndicatorFlags

Specifies the LED indicator that corresponds to the <b>MakeCode</b> scan code. For information about the flags, see the <b>LedFlags</b> member of the <a href="https://msdn.microsoft.com/68c9d24a-c1c9-4ef6-904d-6aeb68cea32a">KEYBOARD_INDICATOR_PARAMETERS</a> structure.


## -remarks



This structure is used with an <a href="https://msdn.microsoft.com/84006453-cf73-44f2-ac8b-ea03382e113d">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a> request to obtain indicator translation information.




## -see-also




<a href="https://msdn.microsoft.com/6119ca39-f740-4c8a-a7f1-eb6f30624093">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/3d70b34c-e201-40fc-99dd-cd05bdeec5f8">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://msdn.microsoft.com/84006453-cf73-44f2-ac8b-ea03382e113d">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/0c19670b-0440-4a7a-ad87-a97d3da28e74">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/25631717-8aee-4eac-8337-46b13aa714a4">IOCTL_KEYBOARD_SET_INDICATORS</a>



<a href="https://msdn.microsoft.com/27c538dd-19e2-4b5a-9605-0efb0f78e008">IOCTL_KEYBOARD_SET_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/68c9d24a-c1c9-4ef6-904d-6aeb68cea32a">KEYBOARD_INDICATOR_PARAMETERS</a>
 

 

