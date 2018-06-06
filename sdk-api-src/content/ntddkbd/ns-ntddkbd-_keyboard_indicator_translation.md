---
UID: NS:ntddkbd._KEYBOARD_INDICATOR_TRANSLATION
title: "_KEYBOARD_INDICATOR_TRANSLATION"
author: windows-sdk-content
description: KEYBOARD_INDICATOR_TRANSLATION specifies a device-specific, variable length array of mappings between keyboard scan codes and LED indicators.
old-location: hid\keyboard_indicator_translation.htm
old-project: hid
ms.assetid: 7ee6ab87-b8fa-4d2c-a51f-5a20ed836d6a
ms.author: windowssdkdev
ms.date: 04/30/2018
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
tech.root: 
req.typenames: KEYBOARD_INDICATOR_TRANSLATION, *PKEYBOARD_INDICATOR_TRANSLATION
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
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _KEYBOARD_INDICATOR_TRANSLATION structure


## -description


KEYBOARD_INDICATOR_TRANSLATION specifies a device-specific, variable length array of mappings between keyboard scan codes and LED indicators.


## -struct-fields




### -field NumberOfIndicatorKeys

Specifies the number of elements in the <b>IndicatorList</b> array.


### -field IndicatorList

Specifies a device-specific, variable-length array of INDICATOR_LIST structures.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef struct _INDICATOR_LIST {
  USHORT  MakeCode;
  USHORT  IndicatorFlags;
} INDICATOR_LIST, *PINDICATOR_LIST;</pre>
</td>
</tr>
</table></span></div>




#### MakeCode

Specifies the make scan code that is generated when a key is pressed.



#### IndicatorFlags

Specifies the LED indicator that corresponds to the <b>MakeCode</b> scan code. For information about the flags, see the <b>LedFlags</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff542331">KEYBOARD_INDICATOR_PARAMETERS</a> structure.


## -remarks



This structure is used with an <a href="https://msdn.microsoft.com/library/windows/hardware/ff541349">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a> request to obtain indicator translation information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541318">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541337">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541349">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541362">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542067">IOCTL_KEYBOARD_SET_INDICATORS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542076">IOCTL_KEYBOARD_SET_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542331">KEYBOARD_INDICATOR_PARAMETERS</a>
 

 

