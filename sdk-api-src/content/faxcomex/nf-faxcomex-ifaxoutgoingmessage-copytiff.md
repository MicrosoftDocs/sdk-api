---
UID: NF:faxcomex.IFaxOutgoingMessage.CopyTiff
title: IFaxOutgoingMessage::CopyTiff (faxcomex.h)
description: The IFaxOutgoingMessage::CopyTiff method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the outbound fax message, to a file on the local computer.
helpviewer_keywords: ["CopyTiff","CopyTiff method [Fax Service]","CopyTiff method [Fax Service]","IFaxOutgoingMessage interface","IFaxOutgoingMessage interface [Fax Service]","CopyTiff method","IFaxOutgoingMessage.CopyTiff","IFaxOutgoingMessage::CopyTiff","_mfax_faxoutgoingmessage.copytiff","fax._mfax_faxoutgoingmessage_copytiff","fax._mfax_faxoutgoingmessage_cpp_mfax_faxoutgoingmessage_copytiff_cpp","faxcomex/IFaxOutgoingMessage::CopyTiff"]
old-location: fax\_mfax_faxoutgoingmessage_cpp_mfax_faxoutgoingmessage_copytiff_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_19eu.htm
ms.date: 12/05/2018
ms.keywords: CopyTiff, CopyTiff method [Fax Service], CopyTiff method [Fax Service],IFaxOutgoingMessage interface, IFaxOutgoingMessage interface [Fax Service],CopyTiff method, IFaxOutgoingMessage.CopyTiff, IFaxOutgoingMessage::CopyTiff, _mfax_faxoutgoingmessage.copytiff, fax._mfax_faxoutgoingmessage_copytiff, fax._mfax_faxoutgoingmessage_cpp_mfax_faxoutgoingmessage_copytiff_cpp, faxcomex/IFaxOutgoingMessage::CopyTiff
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxOutgoingMessage::CopyTiff
 - faxcomex/IFaxOutgoingMessage::CopyTiff
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutgoingMessage.CopyTiff
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> or <b>farMANAGE_OUT_ARCHIVE</b> access right.

With the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> access right, users will be able to use this method only for their own faxes. With the <b>farMANAGE_OUT_ARCHIVE</b> access right, users will be able to use this method for all faxes on the server.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage">FaxOutgoingMessage</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessage">IFaxOutgoingMessage</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-outgoing-archive">Visual Basic Example</a>