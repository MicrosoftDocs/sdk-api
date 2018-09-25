---
UID: NS:tapi.phonemessage_tag
title: phonemessage_tag
author: windows-sdk-content
description: The PHONEMESSAGE structure contains the next message queued for delivery to the application. The phoneGetMessage function returns this structure.
old-location: tapi2\phonemessage_str.htm
tech.root: tapi
ms.assetid: 3655efef-d24c-4d67-b1dc-29d1948a1869
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*LPPHONEMESSAGE, LPPHONEMESSAGE, LPPHONEMESSAGE structure pointer [TAPI 2.2], PHONEMESSAGE, PHONEMESSAGE structure [TAPI 2.2], _tapi2_phonemessage_str, phonemessage_tag, tapi/LPPHONEMESSAGE, tapi/PHONEMESSAGE, tapi2.phonemessage_str"
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - PHONEMESSAGE
product: Windows
targetos: Windows
req.typenames: PHONEMESSAGE, *LPPHONEMESSAGE
req.redist: 
---

# phonemessage_tag structure


## -description


The 
<b>PHONEMESSAGE</b> structure contains the next message queued for delivery to the application. The 
<a href="https://msdn.microsoft.com/8afa17ef-a47f-41af-b120-1e2d5acb4106">phoneGetMessage</a> function returns this structure.


## -struct-fields




### -field hDevice

Handle to a phone device.


### -field dwMessageID

Phone message.


### -field dwCallbackInstance

Instance data passed back to the application, which was specified by the application in 
<a href="https://msdn.microsoft.com/362e37df-4b14-4651-8d23-b70613e354c8">phoneInitializeEx</a>. This value is not interpreted by TAPI.


### -field dwParam1

Parameter for the message.


### -field dwParam2

Parameter for the message.


### -field dwParam3

Parameter for the message.


## -remarks



For information about parameter values passed in this structure, see 
<a href="https://msdn.microsoft.com/b84c77ae-5d0f-416c-83c5-f7874168d996">Phone Device Messages</a>.




## -see-also




<a href="https://msdn.microsoft.com/8afa17ef-a47f-41af-b120-1e2d5acb4106">phoneGetMessage</a>



<a href="https://msdn.microsoft.com/362e37df-4b14-4651-8d23-b70613e354c8">phoneInitializeEx</a>
 

 

