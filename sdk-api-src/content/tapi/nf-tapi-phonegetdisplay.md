---
UID: NF:tapi.phoneGetDisplay
title: phoneGetDisplay function (tapi.h)
author: windows-sdk-content
description: The phoneGetDisplay function returns the current contents of the specified phone display.
old-location: tapi2\phonegetdisplay.htm
tech.root: Tapi
ms.assetid: f9176550-f48a-451d-be98-ad4bd593276b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_tapi2_phonegetdisplay, phoneGetDisplay, phoneGetDisplay function [TAPI 2.2], tapi/phoneGetDisplay, tapi2.phonegetdisplay"
ms.topic: function
f1_keywords: 
 - "tapi/phoneGetDisplay"
dev_langs:
 - c++
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
 - phoneGetDisplay
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a>.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPOINTER, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONESTATE, PHONEERR_STRUCTURETOOSMALL, PHONEERR_OPERATIONUNAVAIL, PHONEERR_UNINITIALIZED, PHONEERR_NOMEM.




## -remarks



The <b>lpDisplay</b> memory area should be at least (<b>dwDisplayNumRows</b> * <b>dwDisplayNumColumns</b>) elements in size to receive all of the display information. The <b>dwDisplayNumRows</b> and <b>dwDisplayNumColumns</b> members are available in the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a> structure returned by 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-phonegetdevcaps">phoneGetDevCaps</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-phonegetdevcaps">phoneGetDevCaps</a>
 

 

