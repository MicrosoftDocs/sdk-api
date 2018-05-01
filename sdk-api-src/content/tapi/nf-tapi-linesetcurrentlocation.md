---
UID: NF:tapi.lineSetCurrentLocation
title: lineSetCurrentLocation function
author: windows-driver-content
description: The lineSetCurrentLocation function sets the location used as the context for address translation.
old-location: tapi2\linesetcurrentlocation.htm
old-project: Tapi
ms.assetid: ad31bc8b-399d-4c2e-b79c-fc935d5adf1a
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: "_tapi2_linesetcurrentlocation, lineSetCurrentLocation, lineSetCurrentLocation function [TAPI 2.2], tapi/lineSetCurrentLocation, tapi2.linesetcurrentlocation"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: FLICK_POINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tapi32.dll
api_name:
-	lineSetCurrentLocation
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineSetCurrentLocation function


## -description


The 
<b>lineSetCurrentLocation</b> function sets the location used as the context for address translation.


## -parameters




### -param hLineApp

Application handle returned by 
<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>. If an application has not yet called the 
<b>lineInitializeEx</b> function, it can set the <i>hLineApp</i> parameter to zero.


### -param dwLocation

New value for the CurrentLocation entry in the [Locations] section in the registry. It must contain a valid permanent identifier of a Location entry in the [Locations] section, as obtained from 
<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">lineGetTranslateCaps</a>. If it is valid, the CurrentLocation entry is updated.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INIFILECORRUPT, LINEERR_NOMEM, LINEERR_INVALAPPHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALLOCATION, LINEERR_RESOURCEUNAVAIL, LINEERR_NODRIVER, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">lineGetTranslateCaps</a>



<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>
 

 

