---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _KEYBOARD_ATTRIBUTES structure


## -description


KEYBOARD_ATTRIBUTES specifies the attributes of a keyboard.


## -struct-fields




### -field KeyboardIdentifier

Specifies the keyboard type and subtype in a KEYBOARD_ID structure:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef struct _KEYBOARD_ID {
  UCHAR  Type;
  UCHAR  Subtype;
} KEYBOARD_ID, *PKEYBOARD_ID;</pre>
</td>
</tr>
</table></span></div>




#### Type

Specifies the keyboard type.



#### Subtype

Specifies the keyboard subtype, which is a vendor-specific value.



##### 


### -field KeyboardMode

Specifies the scan code mode. See the Remarks section.


### -field NumberOfFunctionKeys

Specifies the number of function keys that a keyboard supports.


### -field NumberOfIndicators

Specifies the number of LED indicators that a keyboard supports.


### -field NumberOfKeysTotal

Specifies the number of keys that a keyboard supports.


### -field InputDataQueueLength

Specifies the size, in bytes, of the input data queue used by the keyboard port driver.


### -field KeyRepeatMinimum

Specifies the minimum possible value for the keyboard typematic rate and delay in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542346">KEYBOARD_TYPEMATIC_PARAMETERS</a> structure.


### -field KeyRepeatMaximum

Specifies the maximum possible value for the keyboard typematic rate and delay in a KEYBOARD_TYPEMATIC_PARAMETERS structure.


## -remarks



This structure is used with a <a href="https://msdn.microsoft.com/library/windows/hardware/ff541318">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a> request to return information about the attributes that a keyboard supports.

For information about keyboard types, subtypes, scan code modes, and related keyboard layouts, see the documentation in i8042prt.h, kbd.h, and the <a href="http://go.microsoft.com/fwlink/p/?linkid=256128">layout</a> files in the MSDN Code Gallery. See also the Microsoft specification <i>Keyboard Scan Code Specification</i> available at the <a href="http://go.microsoft.com/fwlink/p/?linkid=242210">key support and scan codes</a> website.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541318">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541337">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541349">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541362">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542067">IOCTL_KEYBOARD_SET_INDICATORS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542076">IOCTL_KEYBOARD_SET_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542346">KEYBOARD_TYPEMATIC_PARAMETERS</a>
 

 

