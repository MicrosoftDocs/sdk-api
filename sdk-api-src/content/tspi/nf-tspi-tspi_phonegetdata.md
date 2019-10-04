---
UID: NF:tspi.TSPI_phoneGetData
title: TSPI_phoneGetData function (tspi.h)
author: windows-sdk-content
description: The TSPI_phoneGetData function uploads the information from the specified location in the open phone device to the specified buffer.
old-location: tspi\tspi_phonegetdata.htm
tech.root: Tapi
ms.assetid: 16692dfe-7a78-428a-94c0-bf56dda834b6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TSPI_phoneGetData, TSPI_phoneGetData function [TAPI 2.2], _tspi_tspi_phonegetdata, tspi.tspi_phonegetdata, tspi/TSPI_phoneGetData
ms.topic: function
f1_keywords: 
 - "tspi/TSPI_phoneGetData"
dev_langs:
 - c++
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
 - TSPI_phoneGetData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TSPI_phoneGetData function


## -description


The 
<b>TSPI_phoneGetData</b> function uploads the information from the specified location in the open phone device to the specified buffer.


## -parameters




### -param hdPhone

The handle to the phone to be queried.


### -param dwDataID

Specifies where in the phone device the buffer is to be uploaded from.


### -param lpData

A pointer to the memory buffer where the data is to be uploaded to.


### -param dwSize

The size of the data buffer in bytes. If the <i>lpData</i> parameter is a pointer to a string, the size must include the <b>null</b> terminator.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONUNAVAIL, PHONEERR_INVALDATAID, PHONEERR_RESOURCEUNAVAIL.




## -remarks



The 
<b>TSPI_phoneGetData</b> function uploads a maximum of <i>dwSize</i> bytes from the phone device into <i>lpData</i>. If <i>dwSize</i> is zero, nothing is copied. The size of each data area is listed in the phone's 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdevcaps">TSPI_phoneGetDevCaps</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_phonesetdata">TSPI_phoneSetData</a>
 

 

