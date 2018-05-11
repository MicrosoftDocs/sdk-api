---
UID: NS:tapi.phonebuttoninfo_tag
title: phonebuttoninfo_tag
author: windows-driver-content
description: The PHONEBUTTONINFO structure contains information about a button on a phone device. This structure is used by multiple TAPI and TSPI functions.
old-location: tapi2\phonebuttoninfo_str.htm
old-project: Tapi
ms.assetid: f8316587-f279-419a-a35d-194df3fc8383
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: "*LPPHONEBUTTONINFO, LPPHONEBUTTONINFO, LPPHONEBUTTONINFO structure pointer [TAPI 2.2], PHONEBUTTONINFO, PHONEBUTTONINFO structure [TAPI 2.2], _tapi2_phonebuttoninfo_str, phonebuttoninfo_tag, tapi/LPPHONEBUTTONINFO, tapi/PHONEBUTTONINFO, tapi2.phonebuttoninfo_str"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: tapi.h
req.include-header: 
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
req.typenames: PHONEBUTTONINFO, *LPPHONEBUTTONINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi.h
api_name:
-	PHONEBUTTONINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# phonebuttoninfo_tag structure


## -description


The 
<b>PHONEBUTTONINFO</b> structure contains information about a button on a phone device. This structure is used by multiple TAPI and TSPI functions.


## -struct-fields




### -field dwTotalSize

Total size allocated to this data structure, in bytes.


### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.


### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.


### -field dwButtonMode

Mode or general usage class of the button. This member uses one of the 
<a href="https://msdn.microsoft.com/7bf337ee-acda-42fe-b50b-370aad50dc03">PHONEBUTTONMODE_ Constants</a>.


### -field dwButtonFunction

Function assigned to the button. This member uses one of the 
<a href="https://msdn.microsoft.com/33d369d0-2221-403e-8fbc-a9a1cbd640ad">PHONEBUTTONFUNCTION_ Constants</a>.


### -field dwButtonTextSize

Size of the descriptive text for the button, in bytes.


### -field dwButtonTextOffset

Offset from the beginning of this structure to the variably sized field containing descriptive text for this button. The format of this information is as specified in the <b>dwStringFormat</b> member of the phone's device capabilities. The size of the field is specified by <b>dwButtonTextSize</b>.


### -field dwDevSpecificSize

Size of the device-specific field, in bytes. If the device-specific field is a pointer to a string, the size must include the <b>null</b> terminator.


### -field dwDevSpecificOffset

Offset from the beginning of the structure to the variably sized device-specific field. The size of the field is specified by <b>dwDevSpecificSize</b>.


### -field dwButtonState

For the 
<a href="https://msdn.microsoft.com/a4df5ba0-7fce-4d29-80a6-4f8f58ae1a83">phoneGetButtonInfo</a> function, this field indicates the current state of the button, using the 
<a href="https://msdn.microsoft.com/f1196e31-65c6-4ade-a0b7-c7758ce97be1">PHONEBUTTONSTATE_ Constants</a>. This field is ignored by the 
<a href="https://msdn.microsoft.com/f51581a9-7b2a-4ba0-83fa-f464c8202648">phoneSetButtonInfo</a> function.


## -remarks



Device-specific extensions should use the DevSpecific (<b>dwDevSpecificSize</b> and <b>dwDevSpecificOffset</b>) variably sized area of this data structure.

Older applications are compiled without this field in the 
<b>PHONEBUTTONINFO</b> structure, and using a SIZEOF PHONEBUTTONINFO smaller than the new size. The application passes in a <i>dwAPIVersion</i> parameter with the 
<a href="https://msdn.microsoft.com/8fba6d5e-0d8c-488f-a17c-4852b487e300">phoneOpen</a> function, which can be used for guidance by TAPI in handling this situation. If the application passes in a <b>dwTotalSize</b> less than the size of the fixed portion of the structure as defined in the specified <b>dwAPIVersion</b>, PHONEERR_STRUCTURETOOSMALL is returned. If sufficient memory has been allocated by the application, before calling the 
<a href="https://msdn.microsoft.com/b4db8075-1e45-4662-805c-6e3004517374">TSPI_phoneGetButtonInfo</a> function, TAPI sets the <b>dwNeededSize</b> and <b>dwUsedSize</b> members to the fixed size of the structure as it existed in the specified API version.

New service providers (which support the new API version) must examine the API version passed in. If the API version is less than the highest version supported by the provider, the service provider must not fill in fields not supported in older API versions, as these would fall in the variable portion of the older structure.

New applications must be cognizant of the API version negotiated, and not examine the contents of fields in the fixed portion beyond the original end of the fixed portion of the structure for the negotiated API version.




## -see-also




<a href="https://msdn.microsoft.com/b4db8075-1e45-4662-805c-6e3004517374">TSPI_phoneGetButtonInfo</a>



<a href="https://msdn.microsoft.com/33b01ac2-cbfd-4697-b242-a7a8f5d1b256">TSPI_phoneSetButtonInfo</a>



<a href="https://msdn.microsoft.com/a4df5ba0-7fce-4d29-80a6-4f8f58ae1a83">phoneGetButtonInfo</a>



<a href="https://msdn.microsoft.com/8fba6d5e-0d8c-488f-a17c-4852b487e300">phoneOpen</a>



<a href="https://msdn.microsoft.com/f51581a9-7b2a-4ba0-83fa-f464c8202648">phoneSetButtonInfo</a>
 

 

