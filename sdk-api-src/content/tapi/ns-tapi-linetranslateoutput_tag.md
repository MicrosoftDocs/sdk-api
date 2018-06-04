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

# linetranslateoutput_tag structure


## -description


The 
<b>LINETRANSLATEOUTPUT</b> structure describes the result of an address translation. The 
<a href="https://msdn.microsoft.com/0347d526-9596-4b42-8075-07318bf39634">lineTranslateAddress</a> function uses this structure.


## -struct-fields




### -field dwTotalSize

Total size allocated to this data structure, in bytes.


### -field dwNeededSize

Size needed for this data structure to hold all the returned information, in bytes.


### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.


### -field dwDialableStringSize

Size dialable string, in bytes, including the terminating <b>NULL</b>.


### -field dwDialableStringOffset

Offset from the beginning of this structure to the translated output that can be passed to the 
<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a>, 
<a href="https://msdn.microsoft.com/111e6c11-67a7-4aab-81dd-f1b4316887e7">lineDial</a>, or other function requiring a dialable string. The output is always a <b>null</b>-terminated string. Ancillary fields such as name and subaddress are included in this output string if they were in the input string. This string may contain private information such as calling card numbers. It should not be displayed to the user, to prevent inadvertent visibility to unauthorized persons. The size of the field is specified by <b>dwDialableStringSize</b>.


### -field dwDisplayableStringSize

Size of the translated output that can be displayed to the user, including the <b>null</b> terminator, in bytes.
					


### -field dwDisplayableStringOffset

Offset to the translated output that can be displayed to the user for confirmation. It is identical to <b>DialableString</b>, except the calling card digits are replaced with the friendly name of the card enclosed within bracket characters (for example, "[AT&amp;T Card]"), and ancillary fields such as name and subaddress are removed. Use an appropriate message in <b>dwDisplayableStringOffset</b>, because the string might be displayed publicly in the call-status dialog box. This information is also appropriate to include in call logs. The size of the field is specified by <b>dwDisplayableStringSize</b>.


### -field dwCurrentCountry

Country or region code configured in <b>CurrentLocation</b>. This value may be used to control the display by the application of certain user interface elements, for local call progress tone detection, and for other purposes.


### -field dwDestCountry

Destination country/region code of the translated address. This value may be passed to the <i>dwCountryCode</i> parameter of 
<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a> and other dialing functions (so that the call progress tones of the destination country/region such as a busy signal are properly detected). This field is set to zero if the destination address passed to 
<a href="https://msdn.microsoft.com/0347d526-9596-4b42-8075-07318bf39634">lineTranslateAddress</a> is not in canonical format.


### -field dwTranslateResults

Information derived from the translation process, which may assist the application in presenting user-interface elements. This field uses one of the 
<a href="https://msdn.microsoft.com/7b834c57-d862-4fe6-828c-9e8fa20f3ec7">LINETRANSLATERESULT_ Constants</a>.


## -remarks



This structure cannot be extended.




## -see-also




<a href="https://msdn.microsoft.com/111e6c11-67a7-4aab-81dd-f1b4316887e7">lineDial</a>



<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a>



<a href="https://msdn.microsoft.com/0347d526-9596-4b42-8075-07318bf39634">lineTranslateAddress</a>
 

 

