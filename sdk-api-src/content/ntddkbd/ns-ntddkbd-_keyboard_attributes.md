---
UID: NS:ntddkbd._KEYBOARD_ATTRIBUTES
title: "_KEYBOARD_ATTRIBUTES"
author: windows-sdk-content
description: KEYBOARD_ATTRIBUTES specifies the attributes of a keyboard.
old-location: hid\keyboard_attributes.htm
tech.root: hid
ms.assetid: 060e93de-b84e-4755-a5f8-cbc52d900310
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PKEYBOARD_ATTRIBUTES, KEYBOARD_ATTRIBUTES, KEYBOARD_ATTRIBUTES structure [Human Input Devices], PKEYBOARD_ATTRIBUTES, PKEYBOARD_ATTRIBUTES structure pointer [Human Input Devices], _KEYBOARD_ATTRIBUTES, hid.keyboard_attributes, kref_430bedf0-40bc-4d93-b382-3fe4c69fcbb5.xml, ntddkbd/KEYBOARD_ATTRIBUTES, ntddkbd/PKEYBOARD_ATTRIBUTES"
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
 - KEYBOARD_ATTRIBUTES
product: Windows
targetos: Windows
req.typenames: KEYBOARD_ATTRIBUTES, *PKEYBOARD_ATTRIBUTES
req.redist: 
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

Specifies the minimum possible value for the keyboard typematic rate and delay in a <a href="https://msdn.microsoft.com/4bbf1699-1ba9-4569-97ac-156a91405586">KEYBOARD_TYPEMATIC_PARAMETERS</a> structure.


### -field KeyRepeatMaximum

Specifies the maximum possible value for the keyboard typematic rate and delay in a KEYBOARD_TYPEMATIC_PARAMETERS structure.


## -remarks



This structure is used with a <a href="https://msdn.microsoft.com/6119ca39-f740-4c8a-a7f1-eb6f30624093">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a> request to return information about the attributes that a keyboard supports.

For information about keyboard types, subtypes, scan code modes, and related keyboard layouts, see the documentation in i8042prt.h, kbd.h, and the <a href="http://go.microsoft.com/fwlink/p/?linkid=256128">layout</a> files in the MSDN Code Gallery. See also the Microsoft specification <i>Keyboard Scan Code Specification</i> available at the <a href="http://go.microsoft.com/fwlink/p/?linkid=242210">key support and scan codes</a> website.




## -see-also




<a href="https://msdn.microsoft.com/6119ca39-f740-4c8a-a7f1-eb6f30624093">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/3d70b34c-e201-40fc-99dd-cd05bdeec5f8">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://msdn.microsoft.com/84006453-cf73-44f2-ac8b-ea03382e113d">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/0c19670b-0440-4a7a-ad87-a97d3da28e74">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/25631717-8aee-4eac-8337-46b13aa714a4">IOCTL_KEYBOARD_SET_INDICATORS</a>



<a href="https://msdn.microsoft.com/27c538dd-19e2-4b5a-9605-0efb0f78e008">IOCTL_KEYBOARD_SET_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/4bbf1699-1ba9-4569-97ac-156a91405586">KEYBOARD_TYPEMATIC_PARAMETERS</a>
 

 

