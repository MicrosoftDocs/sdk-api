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

# FWPM_VSWITCH_EVENT0_ structure


## -description


The <b>FWPM_VSWITCH_EVENT0</b> structure contains information about a vSwitch event.


## -struct-fields




### -field eventType

Type: <b><a href="https://msdn.microsoft.com/1c421152-1085-4cf4-ab8c-631a2b800ec8">FWPM_VSWITCH_EVENT_TYPE</a></b>

 The type of vSwitch event.


### -field vSwitchId

Type: <b>wchar_t*</b>

 GUID which identifies a vSwitch.


### -field positionInfo

 


### -field positionInfo.numvSwitchFilterExtensions

 


### -field positionInfo.vSwitchFilterExtensions

 


### -field reorderInfo

 


### -field reorderInfo.inRequiredPosition

 


### -field reorderInfo.numvSwitchFilterExtensions

 


### -field reorderInfo.vSwitchFilterExtensions

 




#### - ( unnamed union )

switch_is(eventType), switch_type(FWPM_VSWITCH_EVENT_TYPE)



#### positionInfo

 Available when <b>eventType</b> is <b>FWPM_VSWITCH_EVENT_FILTER_ADD_TO_FILTER_ENGINE_NOT_IN_REQUIRED_POSITION</b>.



##### numvSwitchFilterExtensions

<b>Type: <b>ULONG</b>
</b>
The number of vSwitch filter extensions.



##### vSwitchFilterExtensions

<b>Type: <b>LPWSTR*</b>
</b>
size_is(numvSwitchFilterExtensions)

Array of strings identifying other vSwitch extensions.



#### reorderInfo

 Available when <b>eventType</b> is <b>FWPM_VSWITCH_EVENT_FILTER_ENGINE_REORDER</b>.



##### inRequiredPosition

<b>Type: <b>BOOL</b>
</b>
True if the filter engine is in the required position to correctly enforce committed filters; otherwise, false.



##### numvSwitchFilterExtensions

<b>Type: <b>ULONG</b>
</b>
The number of vSwitch filter extensions.



##### vSwitchFilterExtensions

<b>Type: <b>LPWSTR*</b>
</b>
size_is(numvSwitchFilterExtensions)

Array of strings identifying other vSwitch extensions.


## -remarks



<b>FWPM_VSWITCH_EVENT0</b> is a specific implementation of FWPM_VSWITCH_EVENT. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/1c421152-1085-4cf4-ab8c-631a2b800ec8">FWPM_VSWITCH_EVENT_TYPE</a>
 

 

