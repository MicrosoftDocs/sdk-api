---
UID: NF:tspi.TSPI_phoneSetLamp
title: TSPI_phoneSetLamp function
author: windows-sdk-content
description: The TSPI_phoneSetLamp function causes the specified lamp to be set on the specified open phone device in the specified lamp mode.
old-location: tspi\tspi_phonesetlamp.htm
old-project: Tapi
ms.assetid: d525b5d2-f5f8-490b-9db8-06881060efe5
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: TSPI_phoneSetLamp, TSPI_phoneSetLamp function [TAPI 2.2], _tspi_tspi_phonesetlamp, tspi.tspi_phonesetlamp, tspi/TSPI_phoneSetLamp
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AAAccountingData
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_phoneSetLamp
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_phoneSetLamp function


## -description


The 
<b>TSPI_phoneSetLamp</b> function causes the specified lamp to be set on the specified open phone device in the specified lamp mode.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdPhone

The handle to the phone whose lamp is to be set.


### -param dwButtonLampID

The button whose lamp is to be set.


### -param dwLampMode

Specifies how the lamp is to be lit. The <i>dwLampMode</i> parameter can only have one of the 
<a href="https://msdn.microsoft.com/4f6ed2fa-32c9-44b4-bfb5-2c1446ea84fe">PHONELAMPMODE_ constants</a>.


## -returns



Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds or it is an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALBUTTONLAMPID, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALLAMPMODE, PHONEERR_OPERATIONUNAVAIL.




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/4f6ed2fa-32c9-44b4-bfb5-2c1446ea84fe">PHONELAMPMODE_ Constants</a>



<a href="https://msdn.microsoft.com/d929ed39-ba1d-4eae-9667-86d904ba96a8">TSPI_phoneGetDevCaps</a>



<a href="https://msdn.microsoft.com/121032ec-e9ec-4896-b114-3db2b3336812">TSPI_phoneGetLamp</a>
 

 

