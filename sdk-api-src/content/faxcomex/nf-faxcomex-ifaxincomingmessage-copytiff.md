---
UID: NF:faxcomex.IFaxIncomingMessage.CopyTiff
title: IFaxIncomingMessage::CopyTiff
author: windows-sdk-content
description: The CopyTiff method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the inbound fax message to a file on the local computer.
old-location: fax\_mfax_faxincomingmessage_copytiff_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1vc6.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: CopyTiff, CopyTiff method [Fax Service], CopyTiff method [Fax Service],FaxIncomingMessage object, FaxIncomingMessage object [Fax Service],CopyTiff method, FaxIncomingMessage.CopyTiff, IFaxIncomingMessage.CopyTiff, IFaxIncomingMessage::CopyTiff, _mfax_faxincomingmessage.copytiff, fax._mfax_faxincomingmessage_copytiff, fax._mfax_faxincomingmessage_copytiff_vb
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
 - FaxIncomingMessage.CopyTiff
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxIncomingMessage::CopyTiff


## -description


The <b>CopyTiff</b> method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the inbound fax message to a file on the local computer.


## -parameters




### -param bstrTiffPath [in]

Type: <b>String</b>

Null-terminated <b>String</b> that specifies a fully qualified path and file name on the local computer. The fax service will copy the TIFF Class F file associated with the inbound fax message to the specified file.


## -see-also




<a href="https://msdn.microsoft.com/library/ms686126(v=VS.85).aspx">FaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/library/ms686128(v=VS.85).aspx">IFaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/library/ms693406(v=VS.85).aspx">Visual Basic Example</a>
 

 

