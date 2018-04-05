---
UID: NF:tapi.phoneGetDisplay
title: phoneGetDisplay function
author: windows-driver-content
description: The phoneGetDisplay function returns the current contents of the specified phone display.
old-location: tapi2\phonegetdisplay.htm
old-project: Tapi
ms.assetid: f9176550-f48a-451d-be98-ad4bd593276b
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "_tapi2_phonegetdisplay, phoneGetDisplay, phoneGetDisplay function [TAPI 2.2], tapi/phoneGetDisplay, tapi2.phonegetdisplay"
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
-	phoneGetDisplay
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneGetDisplay function


## -description


The 
<b>phoneGetDisplay</b> function returns the current contents of the specified phone display.


## -parameters




### -param hPhone

Handle to the open phone device.


### -param lpDisplay

Pointer to the memory location where the display content is to be stored, of type 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a>.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPOINTER, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONESTATE, PHONEERR_STRUCTURETOOSMALL, PHONEERR_OPERATIONUNAVAIL, PHONEERR_UNINITIALIZED, PHONEERR_NOMEM.




## -remarks



The <b>lpDisplay</b> memory area should be at least (<b>dwDisplayNumRows</b> * <b>dwDisplayNumColumns</b>) elements in size to receive all of the display information. The <b>dwDisplayNumRows</b> and <b>dwDisplayNumColumns</b> members are available in the 
<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a> structure returned by 
<a href="https://msdn.microsoft.com/7bfef6d7-d5fd-4887-afb8-b1d850df050d">phoneGetDevCaps</a>.




## -see-also




<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>



<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a>



<a href="https://msdn.microsoft.com/7bfef6d7-d5fd-4887-afb8-b1d850df050d">phoneGetDevCaps</a>
 

 

