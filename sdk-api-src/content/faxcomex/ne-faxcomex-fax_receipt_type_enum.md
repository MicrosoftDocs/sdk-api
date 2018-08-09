---
UID: NE:faxcomex.FAX_RECEIPT_TYPE_ENUM
title: FAX_RECEIPT_TYPE_ENUM
author: windows-sdk-content
description: The FAX_RECEIPT_TYPE_ENUM enumeration defines the types of delivery reports (delivery receipt formats) for outbound faxes. The members of this enumeration are bit values and can be used in combination.
old-location: fax\_mfax_fax_receipt_type_enum.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_1igd.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FAX_RECEIPT_TYPE_ENUM, FAX_RECEIPT_TYPE_ENUM enumeration [Fax Service], _mfax_fax_receipt_type_enum, fax._mfax_fax_receipt_type_enum, faxcomex/FAX_RECEIPT_TYPE_ENUM, faxcomex/frtMAIL, faxcomex/frtMSGBOX, faxcomex/frtNONE, frtMAIL, frtMSGBOX, frtNONE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: FAX_RECEIPT_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_RECEIPT_TYPE_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
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
 

 

