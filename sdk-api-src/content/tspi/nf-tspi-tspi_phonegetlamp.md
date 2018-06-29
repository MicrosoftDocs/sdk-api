---
UID: NF:tspi.TSPI_phoneGetLamp
title: TSPI_phoneGetLamp function
author: windows-sdk-content
description: The TSPI_phoneGetLamp function returns the current lamp mode of the specified lamp.
old-location: tspi\tspi_phonegetlamp.htm
old-project: Tapi
ms.assetid: 121032ec-e9ec-4896-b114-3db2b3336812
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: TSPI_phoneGetLamp, TSPI_phoneGetLamp function [TAPI 2.2], _tspi_tspi_phonegetlamp, tspi.tspi_phonegetlamp, tspi/TSPI_phoneGetLamp
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
 - TSPI_phoneGetLamp
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_phoneGetLamp function


## -description


The 
<b>TSPI_phoneGetLamp</b> function returns the current lamp mode of the specified lamp.


## -parameters




### -param hdPhone

The handle to the phone whose lamp mode is to be retrieved.


### -param dwButtonLampID

The identifier of the lamp to be queried.


### -param lpdwLampMode

A pointer to a memory location into which the service provider writes the lamp mode status of the given lamp. This parameter can have at most one of the 
<a href="https://msdn.microsoft.com/4f6ed2fa-32c9-44b4-bfb5-2c1446ea84fe">PHONELAMPMODE_ constants</a>.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALBUTTONLAMPID, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONEHANDLE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOMEM.




## -remarks



Phone sets that have multiple lamps per button should be modeled using multiple button/lamps pairs. Each additional button/lamp pair should use a DUMMY button.




## -see-also




<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>



<a href="https://msdn.microsoft.com/4f6ed2fa-32c9-44b4-bfb5-2c1446ea84fe">PHONELAMPMODE_ Constants</a>



<a href="https://msdn.microsoft.com/d929ed39-ba1d-4eae-9667-86d904ba96a8">TSPI_phoneGetDevCaps</a>



<a href="https://msdn.microsoft.com/d525b5d2-f5f8-490b-9db8-06881060efe5">TSPI_phoneSetLamp</a>
 

 

