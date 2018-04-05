---
UID: NF:tapi.phoneSetData
title: phoneSetData function
author: windows-driver-content
description: The phoneSetData function downloads the information in the specified buffer to the opened phone device at the selected data identifier.
old-location: tapi2\phonesetdata.htm
old-project: Tapi
ms.assetid: 4563467b-6577-4210-9440-8445e307ac38
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "_tapi2_phonesetdata, phoneSetData, phoneSetData function [TAPI 2.2], tapi/phoneSetData, tapi2.phonesetdata"
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
-	phoneSetData
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneSetData function


## -description


The 
<b>phoneSetData</b> function downloads the information in the specified buffer to the opened phone device at the selected data identifier.


## -parameters




### -param hPhone

Handle to the open phone device. The application must be the owner of the phone.


### -param dwDataID

Where in the phone device the buffer is to be downloaded.


### -param lpData

Pointer to the memory location where the data is to be downloaded from.


### -param dwSize

Size of the buffer, in bytes.


## -returns



Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOTOWNER, PHONEERR_NOMEM, PHONEERR_INVALDATAID, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPOINTER, PHONEERR_UNINITIALIZED.




## -remarks



The 
<b>phoneSetData</b> function downloads a maximum of <i>dwSize</i> bytes from <i>lpData</i> to the phone device. The format of the data, its meaning to the phone device, and the meaning of the data identifier are service provider-specific. The data in the buffer or the selection of a data identifier may act as commands to the phone device.




## -see-also




<a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a>



<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

