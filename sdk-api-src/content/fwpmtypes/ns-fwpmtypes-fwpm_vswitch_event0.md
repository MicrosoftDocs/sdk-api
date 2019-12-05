---
UID: NS:fwpmtypes.FWPM_VSWITCH_EVENT0_
title: FWPM_VSWITCH_EVENT0 (fwpmtypes.h)
description: Contains information about a vSwitch event.
old-location: fwp\fwpm_vswitch_event0.htm
tech.root: fwp
ms.assetid: bd25f66a-511a-470d-a33a-5e73d8b802c2
ms.date: 12/05/2018
ms.keywords: FWPM_VSWITCH_EVENT0, FWPM_VSWITCH_EVENT0 structure [Filtering], fwp.fwpm_vswitch_event0, fwpmtypes/FWPM_VSWITCH_EVENT0
ms.topic: struct
f1_keywords:
- fwpmtypes/FWPM_VSWITCH_EVENT0
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Fwpmtypes.h
api_name:
- FWPM_VSWITCH_EVENT0
targetos: Windows
req.typenames: FWPM_VSWITCH_EVENT0
req.redist: 
ms.custom: 19H1
---

# FWPM_VSWITCH_EVENT0 structure


## -description


The <b>FWPM_VSWITCH_EVENT0</b> structure contains information about a vSwitch event.


## -struct-fields




### -field eventType

Type: [FWPM_VSWITCH_EVENT_TYPE](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)a></b>

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



<b>FWPM_VSWITCH_EVENT0</b> is a specific implementation of FWPM_VSWITCH_EVENT. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




[FWPM_VSWITCH_EVENT_TYPE](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)a>
 

 

