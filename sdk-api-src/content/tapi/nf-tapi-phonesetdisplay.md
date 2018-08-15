---
UID: NF:tapi.phoneSetDisplay
title: phoneSetDisplay function
author: windows-sdk-content
description: The phoneSetDisplay function causes the specified string to be displayed on the specified open phone device.
old-location: tapi2\phonesetdisplay.htm
old-project: tapi
ms.assetid: 154efb07-7c4e-47f0-8a14-e2fe404efcb7
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: "_tapi2_phonesetdisplay, phoneSetDisplay, phoneSetDisplay function [TAPI 2.2], tapi/phoneSetDisplay, tapi2.phonesetdisplay"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: FLICK_POINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - phoneSetDisplay
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneSetDisplay function


## -description


The 
<b>phoneSetDisplay</b> function causes the specified string to be displayed on the specified open phone device.


## -parameters




### -param hPhone

Handle to the open phone device. The application must be the owner of the phone.


### -param dwRow

Row position on the display where the new text is to be displayed.


### -param dwColumn

Column position on the display where the new text is to be displayed.


### -param lpsDisplay

Pointer to the memory location where the display content is stored. The display information must have the format specified in the <b>dwStringFormat</b> member of the 
<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a> structure, which describes the phone's device capabilities.


### -param dwSize

Size of the information pointed to by <i>lpsDisplay</i>, in bytes. If the <i>lpsDisplay</i> parameter is a pointer to a string, the size must include the null terminator.


## -returns



Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOTOWNER, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONESTATE, PHONEERR_UNINITIALIZED, PHONEERR_INVALPOINTER, PHONEERR_NOMEM, PHONEERR_INVALPARAM, PHONEERR_RESOURCEUNAVAIL.




## -remarks



The specified display information is written to the phone's display, starting at the specified positions. This operation overwrites previously displayed information. If the amount of information exceeds the size of the display, the information is truncated. The amount of information that can be displayed is at most (<b>dwNumRows</b> * <b>dwNumColumns</b>) elements in size. <b>dwNumRows</b> and <b>dwNumColumns</b> are available in the 
<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a> structure, which is returned by 
<a href="https://msdn.microsoft.com/7bfef6d7-d5fd-4887-afb8-b1d850df050d">phoneGetDevCaps</a>; they are zero-based. 




## -see-also




<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>



<a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a>



<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/7bfef6d7-d5fd-4887-afb8-b1d850df050d">phoneGetDevCaps</a>
 

 

