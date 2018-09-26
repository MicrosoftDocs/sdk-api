---
UID: NF:faxcomex.IFaxOutgoingMessage.CopyTiff
title: IFaxOutgoingMessage::CopyTiff
author: windows-sdk-content
description: The IFaxOutgoingMessage::CopyTiff method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the outbound fax message, to a file on the local computer.
old-location: fax\_mfax_faxoutgoingmessage_cpp_mfax_faxoutgoingmessage_copytiff_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_19eu.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CopyTiff, CopyTiff method [Fax Service], CopyTiff method [Fax Service],IFaxOutgoingMessage interface, IFaxOutgoingMessage interface [Fax Service],CopyTiff method, IFaxOutgoingMessage.CopyTiff, IFaxOutgoingMessage::CopyTiff, _mfax_faxoutgoingmessage.copytiff, fax._mfax_faxoutgoingmessage_copytiff, fax._mfax_faxoutgoingmessage_cpp_mfax_faxoutgoingmessage_copytiff_cpp, faxcomex/IFaxOutgoingMessage::CopyTiff
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
 - IFaxOutgoingMessage.CopyTiff
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingMessage::CopyTiff


## -description


The <b>IFaxOutgoingMessage::CopyTiff</b> method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the outbound fax message, to a file on the local computer.


## -parameters




### -param bstrTiffPath [in]

Type: <b>BSTR</b>

Null-terminated string that contains a fully qualified path and file name on the local computer. This is the file on the local computer to which the fax service will copy the TIFF Class F file associated with the outbound fax message.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_LOW</a> or <b>farMANAGE_OUT_ARCHIVE</b> access right.

With the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_LOW</a> access right, users will be able to use this method only for their own faxes. With the <b>farMANAGE_OUT_ARCHIVE</b> access right, users will be able to use this method for all faxes on the server.




## -see-also




<a href="https://msdn.microsoft.com/fb06254f-f37b-4783-b4fd-42b5c5a28496">FaxOutgoingMessage</a>



<a href="https://msdn.microsoft.com/7423ccd1-5eb6-402f-99fb-2cbed386450a">IFaxOutgoingMessage</a>



<a href="https://msdn.microsoft.com/072eb2cc-7fd9-4f8e-8583-44384357e708">Visual Basic Example</a>
 

 

