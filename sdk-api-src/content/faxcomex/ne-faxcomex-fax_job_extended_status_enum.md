---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# FAX_JOB_EXTENDED_STATUS_ENUM enumeration


## -description


The <b>FAX_JOB_EXTENDED_STATUS_ENUM</b> enumeration defines the extended status values for a fax job. These are basic values provided for developers of a fax service provider (FSP). However, with the exception of <b><b>fjesPARTIALLY_RECEIVED</b></b>, these values or other proprietary values that may be developed for a specific FSP, are not recognized or interpreted by the fax server.


## -enum-fields




### -field fjesNONE

No extended status value.


### -field fjesDISCONNECTED

The sender or the caller disconnected the fax call.


### -field fjesINITIALIZING

The device is initializing a call.


### -field fjesDIALING

The device is dialing a fax number.


### -field fjesTRANSMITTING

The device is sending a fax.


### -field fjesANSWERED

The device answered a new call.


### -field fjesRECEIVING

The device is receiving a fax.


### -field fjesLINE_UNAVAILABLE

The device is not available because it is in use by another application.


### -field fjesBUSY

The device encountered a busy signal.


### -field fjesNO_ANSWER

The receiving device did not answer the call.


### -field fjesBAD_ADDRESS

The device dialed an invalid fax number.


### -field fjesNO_DIAL_TONE

The sending device cannot complete the call because it does not detect a dial tone.


### -field fjesFATAL_ERROR

The device has encountered a fatal protocol error.


### -field fjesCALL_DELAYED

The device delayed a fax call because the sending device received a busy signal multiple times. The device cannot retry the call because dialing restrictions exist. (Some countries/regions restrict the number of retry attempts when a number is busy.)


### -field fjesCALL_BLACKLISTED

The device could not complete a call because the telephone number was blocked or reserved; emergency numbers such as 911 are blocked. 


### -field fjesNOT_FAX_CALL

The device received a call that was a data call or a voice call.


### -field fjesPARTIALLY_RECEIVED

The incoming fax was partially received. Some (but not all) of the pages are available.


### -field fjesHANDLED

The fax service processed the outbound fax; the fax service provider will transmit the fax.


### -field fjesCALL_COMPLETED

The call was completed.


### -field fjesCALL_ABORTED

The call was aborted.


### -field fjesPROPRIETARY

Obsolete. For information about proprietary extended status codes, see <a href="https://msdn.microsoft.com/f2014b38-b5dd-48bd-a391-457de69bd7b4">IFaxOutgoingJob::get_ExtendedStatusCode</a>.


## -see-also




<a href="https://msdn.microsoft.com/15333cd3-e71a-451c-ae93-9e217ea0895c">ExtendedStatusCode</a>



<a href="https://msdn.microsoft.com/4280eb52-c5fa-4e06-8395-b7039d27eccc">IFaxIncomingJob::get_ExtendedStatus</a>



<a href="https://msdn.microsoft.com/82eb0c39-c61d-4de8-a063-3afeeba5be2e">IFaxJobStatus::get_ExtendedStatus</a>



<a href="https://msdn.microsoft.com/1355f158-8e22-4f25-8ac5-fe81cc175d95">IFaxJobStatus::get_ExtendedStatusCode</a>



<a href="https://msdn.microsoft.com/8b397aa9-aca0-4da2-9afa-cff0933d5f78">IFaxOutgoingJob::get_ExtendedStatus</a>



<a href="https://msdn.microsoft.com/f2014b38-b5dd-48bd-a391-457de69bd7b4">IFaxOutgoingJob::get_ExtendedStatusCode</a>
 

 

