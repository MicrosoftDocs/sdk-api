---
UID: NF:tspi.TSPI_phoneSetButtonInfo
title: TSPI_phoneSetButtonInfo function
author: windows-sdk-content
description: The TSPI_phoneSetButtonInfo function sets information about the specified button on the specified phone.
old-location: tspi\tspi_phonesetbuttoninfo.htm
tech.root: Tapi
ms.assetid: 33b01ac2-cbfd-4697-b242-a7a8f5d1b256
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TSPI_phoneSetButtonInfo, TSPI_phoneSetButtonInfo function [TAPI 2.2], _tspi_tspi_phonesetbuttoninfo, tspi.tspi_phonesetbuttoninfo, tspi/TSPI_phoneSetButtonInfo
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
 - TSPI_phoneSetButtonInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_phoneSetButtonInfo function


## -description


The 
<b>TSPI_phoneSetButtonInfo</b> function sets information about the specified button on the specified phone.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request. The service provider returns this value if the function completes asynchronously.


### -param hdPhone

The handle to the phone for which button info is to be set.


### -param dwButtonLampID

A button on the phone device.


### -param lpButtonInfo

A pointer to a variably sized structure of type 
<a href="https://msdn.microsoft.com/f8316587-f279-419a-a35d-194df3fc8383">PHONEBUTTONINFO</a>. This data structure describes the mode and function, and provides additional descriptive text to be set for the button.


## -returns



Returns the (positive) <i>dwRequestID</i> value if the function is completed asynchronously, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds or it is an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALBUTTONLAMPID, PHONEERR_OPERATIONFAILED, PHONEERR_NOMEM, PHONEERR_OPERATIONUNAVAIL.




## -remarks



This function sets the meaning and associated descriptive text of a phone's buttons.




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/f8316587-f279-419a-a35d-194df3fc8383">PHONEBUTTONINFO</a>



<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>



<a href="https://msdn.microsoft.com/b4db8075-1e45-4662-805c-6e3004517374">TSPI_phoneGetButtonInfo</a>
 

 

