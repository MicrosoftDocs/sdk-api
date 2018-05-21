---
UID: NF:tapi.phoneSetButtonInfo
title: phoneSetButtonInfo function
author: windows-driver-content
description: The phoneSetButtonInfo function sets information about the specified button on the specified phone.
old-location: tapi2\phonesetbuttoninfo.htm
old-project: Tapi
ms.assetid: f51581a9-7b2a-4ba0-83fa-f464c8202648
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: "_tapi2_phonesetbuttoninfo, phoneSetButtonInfo, phoneSetButtonInfo function [TAPI 2.2], phoneSetButtonInfoA, phoneSetButtonInfoW, tapi/phoneSetButtonInfo, tapi/phoneSetButtonInfoA, tapi/phoneSetButtonInfoW, tapi2.phonesetbuttoninfo"
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
req.unicode-ansi: phoneSetButtonInfoW (Unicode) and phoneSetButtonInfoA (ANSI)
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
-	phoneSetButtonInfo
-	phoneSetButtonInfoA
-	phoneSetButtonInfoW
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneSetButtonInfo function


## -description


The 
<b>phoneSetButtonInfo</b> function sets information about the specified button on the specified phone.


## -parameters




### -param hPhone

Handle to the open phone device. The application must be the owner of the phone device.


### -param dwButtonLampID

Button on the phone device.


### -param lpButtonInfo

Pointer to a variably sized structure of type 
<a href="https://msdn.microsoft.com/f8316587-f279-419a-a35d-194df3fc8383">PHONEBUTTONINFO</a>. This data structure describes the mode, the function, and provides additional descriptive text about the button.


## -returns



Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALBUTTONLAMPID, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONEHANDLE, PHONEERR_STRUCTURETOOSMALL, PHONEERR_INVALPOINTER, PHONEERR_UNINITIALIZED, PHONEERR_NOTOWNER, PHONEERR_NOMEM, PHONEERR_OPERATIONUNAVAIL, PHONEERR_RESOURCEUNAVAIL.




## -see-also




<a href="https://msdn.microsoft.com/f8316587-f279-419a-a35d-194df3fc8383">PHONEBUTTONINFO</a>



<a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a>



<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

