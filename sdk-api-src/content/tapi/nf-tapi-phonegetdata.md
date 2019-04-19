---
UID: NF:tapi.phoneGetData
title: phoneGetData function (tapi.h)
author: windows-sdk-content
description: The phoneGetData function uploads the information from the specified location in the open phone device to the specified buffer.
old-location: tapi2\phonegetdata.htm
tech.root: Tapi
ms.assetid: 9ad2f99e-73b3-4e4c-a6cd-49ca0fe775ca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_tapi2_phonegetdata, phoneGetData, phoneGetData function [TAPI 2.2], tapi/phoneGetData, tapi2.phonegetdata"
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
 - phoneGetData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# phoneGetData function


## -description


The 
<b>phoneGetData</b> function uploads the information from the specified location in the open phone device to the specified buffer.


## -parameters




### -param hPhone

Handle to the open phone device.


### -param dwDataID

Where in the phone device the buffer is to be uploaded from.


### -param lpData

Pointer to the memory buffer where the data is to be uploaded.


### -param dwSize

Size of the data buffer, in bytes.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPOINTER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALDATAID, PHONEERR_UNINITIALIZED, PHONEERR_OPERATIONUNAVAIL.




## -remarks



The function uploads a maximum of <i>dwSize</i> bytes from the phone device into the memory area pointed to by <i>lpData</i>. If <i>dwSize</i> is zero, nothing is copied. The size of each data area is listed in the phone's device capabilities.




## -see-also




<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

