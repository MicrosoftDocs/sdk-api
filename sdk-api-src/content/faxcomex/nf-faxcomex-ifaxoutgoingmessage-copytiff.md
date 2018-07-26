---
UID: NF:faxcomex.IFaxOutgoingMessage.CopyTiff
title: IFaxOutgoingMessage::CopyTiff
author: windows-sdk-content
description: The CopyTiff method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the outbound fax message, to a file on the local computer.
old-location: fax\_mfax_faxoutgoingmessage_copytiff_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_19eu.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: CopyTiff, CopyTiff method [Fax Service], CopyTiff method [Fax Service],FaxOutgoingMessage object, FaxOutgoingMessage object [Fax Service],CopyTiff method, FaxOutgoingMessage.CopyTiff, IFaxOutgoingMessage.CopyTiff, IFaxOutgoingMessage::CopyTiff, _mfax_faxoutgoingmessage.copytiff, fax._mfax_faxoutgoingmessage_copytiff, fax._mfax_faxoutgoingmessage_copytiff_vb
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - FaxOutgoingMessage.CopyTiff
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutgoingMessage::CopyTiff


## -description


The <b>CopyTiff</b> method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the outbound fax message, to a file on the local computer.


## -parameters




### -param bstrTiffPath [in]

Type: <b>String</b>

Null-terminated string that contains a fully qualified path and file name on the local computer. This is the file on the local computer to which the fax service will copy the TIFF Class F file associated with the outbound fax message.


## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a> or <b>farMANAGE_OUT_ARCHIVE</b> access right.

With the <a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a> access right, users will be able to use this method only for their own faxes. With the <b>farMANAGE_OUT_ARCHIVE</b> access right, users will be able to use this method for all faxes on the server.




## -see-also




<a href="https://msdn.microsoft.com/library/ms690149(v=VS.85).aspx">FaxOutgoingMessage</a>



<a href="https://msdn.microsoft.com/library/ms690152(v=VS.85).aspx">IFaxOutgoingMessage</a>



<a href="https://msdn.microsoft.com/library/ms693402(v=VS.85).aspx">Visual Basic Example</a>
 

 

