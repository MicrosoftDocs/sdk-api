---
UID: NF:faxcomex.IFaxIncomingMessage.CopyTiff
title: IFaxIncomingMessage::CopyTiff method
author: windows-driver-content
description: The CopyTiff method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the inbound fax message to a file on the local computer.
old-location: fax\_mfax_faxincomingmessage_copytiff_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1vc6.htm
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: CopyTiff method [Fax Service], CopyTiff method [Fax Service], FaxIncomingMessage object, CopyTiff,IFaxIncomingMessage.CopyTiff, FaxIncomingMessage object [Fax Service], CopyTiff method, IFaxIncomingMessage, IFaxIncomingMessage::CopyTiff, _mfax_faxincomingmessage.copytiff, fax._mfax_faxincomingmessage_copytiff, fax._mfax_faxincomingmessage_copytiff_vb
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	FaxIncomingMessage.CopyTiff
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxIncomingMessage::CopyTiff method


## -description


The <b>CopyTiff</b> method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the inbound fax message to a file on the local computer.


## -parameters




### -param bstrTiffPath [in]

Type: <b>String</b>

Null-terminated <b>String</b> that specifies a fully qualified path and file name on the local computer. The fax service will copy the TIFF Class F file associated with the inbound fax message to the specified file.


## -see-also




<a href="https://msdn.microsoft.com/ee546d4c-e580-4738-a5d2-0b10c5d8a1ab">FaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/29fa30c9-d4f2-4ed5-95fc-873f2263c7bb">IFaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/1e66b30d-e74f-4c73-b005-acd2d0fd8893">Visual Basic Example</a>
 

 

