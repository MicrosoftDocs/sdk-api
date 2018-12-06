---
UID: NF:tspi.TSPI_phoneSetDisplay
title: TSPI_phoneSetDisplay function
author: windows-sdk-content
description: The TSPI_phoneSetDisplay function causes the specified string to be displayed on the specified open phone device.
old-location: tspi\tspi_phonesetdisplay.htm
tech.root: tapi
ms.assetid: c320122c-037a-40f5-8314-6aa3352cc994
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TSPI_phoneSetDisplay, TSPI_phoneSetDisplay function [TAPI 2.2], _tspi_tspi_phonesetdisplay, tspi.tspi_phonesetdisplay, tspi/TSPI_phoneSetDisplay
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tspi.h
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
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_phoneSetDisplay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_phoneSetDisplay function


## -description


The 
<b>TSPI_phoneSetDisplay</b> function causes the specified string to be displayed on the specified open phone device.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdPhone

The handle to the phone on which the string is to be displayed.


### -param dwRow

The row on the display where the new text is to be displayed.


### -param dwColumn

The column position on the display where the new text is to be displayed.


### -param lpsDisplay

A pointer to the memory location where the display content is stored. The application stores the display information in the format specified as <b>dwStringFormat</b> in the phone's 
<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a> structure.


### -param dwSize

The size in bytes, including the <b>null</b> terminator, of the information pointed to by <i>lpDisplay</i>.


## -returns



Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds or it is an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPARAM, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOMEM.




## -remarks



The specified display information is written to the phone's display, starting at the specified positions. This operation overwrites previously displayed information. If the amount of information exceeds the size of the display, the information is truncated. The amount of information that can be displayed is at most (<b>dwNumRows</b> * <b>dwNumColumns</b>) elements in size. The <b>dwNumRows</b> and <b>dwNumColumns</b> members are available in the 
<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a> structure returned by 
<a href="https://msdn.microsoft.com/d929ed39-ba1d-4eae-9667-86d904ba96a8">TSPI_phoneGetDevCaps</a>; they are zero-based.




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>



<a href="https://msdn.microsoft.com/d929ed39-ba1d-4eae-9667-86d904ba96a8">TSPI_phoneGetDevCaps</a>



<a href="https://msdn.microsoft.com/dff5fdc5-a627-4282-85d3-2a7ceaf063ed">TSPI_phoneGetDisplay</a>
 

 

