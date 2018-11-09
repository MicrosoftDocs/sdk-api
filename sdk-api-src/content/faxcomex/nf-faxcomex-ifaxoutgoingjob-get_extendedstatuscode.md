---
UID: NF:faxcomex.IFaxOutgoingJob.get_ExtendedStatusCode
title: IFaxOutgoingJob::get_ExtendedStatusCode
author: windows-sdk-content
description: The IFaxOutgoingJob::get_ExtendedStatusCode property specifies a code describing the job's extended status.
old-location: fax\_mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_extendedstatuscode_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_16xx.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: ExtendedStatusCode property [Fax Service], ExtendedStatusCode property [Fax Service],IFaxOutgoingJob interface, IFaxOutgoingJob interface [Fax Service],ExtendedStatusCode property, IFaxOutgoingJob.ExtendedStatusCode, IFaxOutgoingJob.get_ExtendedStatusCode, IFaxOutgoingJob::ExtendedStatusCode, IFaxOutgoingJob::get_ExtendedStatusCode, _mfax_faxoutgoingjob.extendedstatuscode, fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_extendedstatuscode_cpp, fax._mfax_faxoutgoingjob_extendedstatuscode, faxcomex/IFaxOutgoingJob::ExtendedStatusCode, faxcomex/IFaxOutgoingJob::get_ExtendedStatusCode, get_ExtendedStatusCode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutgoingJob.ExtendedStatusCode
 - IFaxOutgoingJob.get_ExtendedStatusCode
 - IFaxOutgoingJob.get_ExtendedStatusCode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingJob::get_ExtendedStatusCode


## -description


The <b>IFaxOutgoingJob::get_ExtendedStatusCode</b> property specifies a code describing the job's extended status.

This property is read-only.


## -parameters


## -remarks



If an fax service provider (FSP) provides a proprietary status code, the service loads the code string from the FSP, and passes both the string and the original status code to the client. If the FSP provides a status defined in <a href="https://msdn.microsoft.com/f0cb862b-cb5c-40bd-9df9-a32f849e45a1">FAX_JOB_EXTENDED_STATUS_ENUM</a>, the service passes only the status code to the client.

A fax client application should check the extended status string first. If the string is not <b>NULL</b>/empty, it describes the extended status, and the extended status code is the same code that the FSP passed to the fax service. If the string is <b>NULL</b>/Empty, the extended status code is one of those defined in <a href="https://msdn.microsoft.com/f0cb862b-cb5c-40bd-9df9-a32f849e45a1">FAX_JOB_EXTENDED_STATUS_ENUM</a>.




## -see-also




<a href="https://msdn.microsoft.com/f9686d11-fd32-4eaf-ae93-399dacf028ac">FaxOutgoingJob</a>



<a href="https://msdn.microsoft.com/3b7c9ecb-0528-4cda-9c9a-cb31e4589c71">IFaxOutgoingJob</a>



<a href="https://msdn.microsoft.com/5fab26c3-99f6-4740-9899-3dccbd26a3ba">Visual Basic Example</a>
 

 

