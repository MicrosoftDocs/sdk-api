---
UID: NF:tspi.TSPI_phoneOpen
title: TSPI_phoneOpen function
author: windows-sdk-content
description: The TSPI_phoneOpen function opens the phone device whose device identifier is given, returning the service provider's opaque handle for the device and retaining TAPI's opaque handle for the device for use in subsequent calls to the PHONEEVENT procedure.
old-location: tspi\tspi_phoneopen.htm
old-project: Tapi
ms.assetid: e2a4372f-62ff-488c-94a7-ed44388b8092
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: TSPI_phoneOpen, TSPI_phoneOpen function [TAPI 2.2], _tspi_tspi_phoneopen, tspi.tspi_phoneopen, tspi/TSPI_phoneOpen
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
 - TSPI_phoneOpen
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_phoneOpen function


## -description


The 
<b>TSPI_phoneOpen</b> function opens the phone device whose device identifier is given, returning the service provider's opaque handle for the device and retaining TAPI's opaque handle for the device for use in subsequent calls to the 
<a href="https://msdn.microsoft.com/0b5745a4-7652-48ce-9e8a-eef52c09455f">PHONEEVENT</a> procedure.


## -parameters




### -param dwDeviceID

The phone device to be opened.


### -param htPhone

The TAPI opaque handle for the phone device to be used in subsequent calls to the 
<a href="https://msdn.microsoft.com/0b5745a4-7652-48ce-9e8a-eef52c09455f">PHONEEVENT</a> callback procedure to identify the device.


### -param lphdPhone

A pointer to an 
<a href="https://msdn.microsoft.com/ad0f398b-c2d1-4f91-b28b-0c4f4c594fc9">HDRVPHONE</a> where the service provider writes its handle for the phone device to be used by TAPI in subsequent calls to identify the device.


### -param dwTSPIVersion

The TSPI version negotiated through 
<a href="https://msdn.microsoft.com/a6bca1a3-a6cd-4cb5-80e9-0da0ad6ba8dc">TSPI_phoneNegotiateTSPIVersion</a> under which the service provider can operate.


### -param lpfnEventProc

A pointer to the 
<a href="https://msdn.microsoft.com/0b5745a4-7652-48ce-9e8a-eef52c09455f">PHONEEVENT</a> callback procedure supplied by TAPI that the service provider calls to report subsequent events on the phone.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_ALLOCATED, PHONEERR_NOMEM, PHONEERR_INCOMPATIBLEAPIVERSION, PHONEERR_RESOURCEUNAVAIL, PHONEERR_NODRIVER, PHONEERR_OPERATIONFAILED, PHONEERR_INUSE, PHONEERR_OPERATIONUNAVAIL, PHONEERR_INIFILECORRUPT.




## -remarks



Opening a phone entitles TAPI to make further requests on the phone. The phone becomes active in the sense that the service provider can report asynchronous events such as hookswitch changes or button presses. The service provider reserves whatever nonsharable resources are required to manage the phone. For example, opening a phone accessed through a comm port and modem should result in opening the comm port, making it no longer available for use by other applications.

If the function succeeds, both TAPI and the service provider become committed to operating under the specified interface version number for this open device. Subsequent operations and events identified using the exchanged opaque phone handles conform to that interface version. This commitment and the validity of the handles remain in effect until TAPI closes the phone using 
<a href="https://msdn.microsoft.com/1db4c460-8afa-4420-9c51-ba276693656e">TSPI_phoneClose</a> or until the service provider reports the 
<a href="https://msdn.microsoft.com/ac9e736c-508b-4048-a958-708264e8045e">PHONE_CLOSE</a> event. If the function is not successful, no such commitment is made and the handles are not valid.




## -see-also




<a href="https://msdn.microsoft.com/0b5745a4-7652-48ce-9e8a-eef52c09455f">PHONEEVENT</a>



<a href="https://msdn.microsoft.com/ac9e736c-508b-4048-a958-708264e8045e">PHONE_CLOSE</a>



<a href="https://msdn.microsoft.com/1db4c460-8afa-4420-9c51-ba276693656e">TSPI_phoneClose</a>



<a href="https://msdn.microsoft.com/a6bca1a3-a6cd-4cb5-80e9-0da0ad6ba8dc">TSPI_phoneNegotiateTSPIVersion</a>
 

 

