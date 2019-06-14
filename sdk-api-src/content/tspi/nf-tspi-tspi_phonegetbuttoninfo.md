---
UID: NF:tspi.TSPI_phoneGetButtonInfo
title: TSPI_phoneGetButtonInfo function (tspi.h)
author: windows-sdk-content
description: The TSPI_phoneGetButtonInfo function returns information about a specified button.
old-location: tspi\tspi_phonegetbuttoninfo.htm
tech.root: Tapi
ms.assetid: b4db8075-1e45-4662-805c-6e3004517374
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TSPI_phoneGetButtonInfo, TSPI_phoneGetButtonInfo function [TAPI 2.2], _tspi_tspi_phonegetbuttoninfo, tspi.tspi_phonegetbuttoninfo, tspi/TSPI_phoneGetButtonInfo
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
 - TSPI_phoneGetButtonInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TSPI_phoneGetButtonInfo function


## -description


The 
<b>TSPI_phoneGetButtonInfo</b> function returns information about a specified button.


## -parameters




### -param hdPhone

The handle to the phone to be queried.


### -param dwButtonLampID

A button on the phone device.


### -param lpButtonInfo

A pointer to memory into which the service provider writes a variably sized structure of type 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-phonebuttoninfo_tag">PHONEBUTTONINFO</a>. This data structure describes the mode and function, and provides additional descriptive text corresponding to the button. Prior to calling 
<b>TSPI_phoneGetButtonInfo</b>, the application sets the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALBUTTONLAMPID, PHONEERR_OPERATIONUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_NOMEM.




## -remarks



The 
<b>TSPI_phoneGetButtonInfo</b> function returns the PHONEERR_NOMEM value if the service provider cannot access the memory containing the button information.

The service provider fills in all the members of the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-phonebuttoninfo_tag">PHONEBUTTONINFO</a> data structure, except for <b>dwTotalSize</b>, which is filled in by TAPI. The service provider must not overwrite the <b>dwTotalSize</b> member.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-phonebuttoninfo_tag">PHONEBUTTONINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-phonecaps_tag">PHONECAPS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_phonesetbuttoninfo">TSPI_phoneSetButtonInfo</a>
 

 

