---
UID: NS:fwpmtypes.FWPM_VSWITCH_EVENT0_
title: FWPM_VSWITCH_EVENT0_
author: windows-sdk-content
description: Contains information about a vSwitch event.
old-location: fwp\fwpm_vswitch_event0.htm
old-project: FWP
ms.assetid: bd25f66a-511a-470d-a33a-5e73d8b802c2
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: FWPM_VSWITCH_EVENT0, FWPM_VSWITCH_EVENT0 structure [Filtering], FWPM_VSWITCH_EVENT0_, fwp.fwpm_vswitch_event0, fwpmtypes/FWPM_VSWITCH_EVENT0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FWPM_VSWITCH_EVENT0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_VSWITCH_EVENT0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
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
 

 

