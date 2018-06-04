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

# FAX_RECEIPT_TYPE_ENUM enumeration


## -description


The <b>FAX_RECEIPT_TYPE_ENUM</b> enumeration defines the types of delivery reports (delivery receipt formats) for outbound faxes. The members of this enumeration are bit values and can be used in combination.


## -enum-fields




### -field frtNONE

Do not send a delivery report.


### -field frtMAIL

Send a delivery report through SMTP mail.


### -field frtMSGBOX

Display a delivery report in a message box on the display of a specific computer. This is not supported in Windows Vista.


## -see-also




<a href="https://msdn.microsoft.com/ee8f9070-7f00-4bd4-8022-1d9b00f1bdaa">IFaxDocument::get_ReceiptType</a>



<a href="https://msdn.microsoft.com/675fa0b8-758d-43b4-b493-ee8204f4b9c6">IFaxOutgoingJob::get_ReceiptType</a>
 

 

