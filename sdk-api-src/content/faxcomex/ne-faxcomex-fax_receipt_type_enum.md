---
UID: NE:faxcomex.FAX_RECEIPT_TYPE_ENUM
title: FAX_RECEIPT_TYPE_ENUM
author: windows-sdk-content
description: The FAX_RECEIPT_TYPE_ENUM enumeration defines the types of delivery reports (delivery receipt formats) for outbound faxes. The members of this enumeration are bit values and can be used in combination.
old-location: fax\_mfax_fax_receipt_type_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_1igd.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: FAX_RECEIPT_TYPE_ENUM
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/ms686899(v=VS.85).aspx">IFaxDocument::get_ReceiptType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689599(v=VS.85).aspx">IFaxOutgoingJob::get_ReceiptType</a>
 

 

