---
UID: NF:tapi.phoneSetLamp
title: phoneSetLamp function (tapi.h)
author: windows-sdk-content
description: The phoneSetLamp function causes the specified lamp to be lit on the specified open phone device in the specified lamp mode.
old-location: tapi2\phonesetlamp.htm
tech.root: Tapi
ms.assetid: 2e21ef29-9c40-4463-8678-028a8772a494
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_tapi2_phonesetlamp, phoneSetLamp, phoneSetLamp function [TAPI 2.2], tapi/phoneSetLamp, tapi2.phonesetlamp"
ms.topic: function
f1_keywords: 
 - "tapi/phoneSetLamp"
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - phoneSetLamp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# phoneSetLamp function


## -description


The 
<b>phoneSetLamp</b> function causes the specified lamp to be lit on the specified open phone device in the specified lamp mode.


## -parameters




### -param hPhone

Handle to the open phone device. The application must be the owner of the phone.


### -param dwButtonLampID

Button whose lamp is to be lit.


### -param dwLampMode

How the lamp is to be lit. This parameter uses one and only one of the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/phonelampmode--constants">PHONELAMPMODE_ Constants</a>.


## -returns



Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding <a href="https://docs.microsoft.com/windows/desktop/Tapi/phone-reply">PHONE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOTOWNER, PHONEERR_NOMEM, PHONEERR_INVALBUTTONLAMPID, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALLAMPMODE, PHONEERR_UNINITIALIZED.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/phone-reply">PHONE_REPLY</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>
 

 

