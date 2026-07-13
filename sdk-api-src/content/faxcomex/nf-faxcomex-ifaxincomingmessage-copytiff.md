---
UID: NF:faxcomex.IFaxIncomingMessage.CopyTiff
title: IFaxIncomingMessage::CopyTiff (faxcomex.h)
description: The CopyTiff method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the inbound fax message to a file on the local computer.
helpviewer_keywords: ["CopyTiff","CopyTiff method [Fax Service]","CopyTiff method [Fax Service]","IFaxIncomingMessage interface","IFaxIncomingMessage interface [Fax Service]","CopyTiff method","IFaxIncomingMessage.CopyTiff","IFaxIncomingMessage::CopyTiff","_mfax_faxincomingmessage.copytiff","fax._mfax_faxincomingmessage_copytiff","fax._mfax_faxincomingmessage_cpp_mfax_faxincomingmessage_copytiff_cpp","faxcomex/IFaxIncomingMessage::CopyTiff"]
old-location: fax\_mfax_faxincomingmessage_cpp_mfax_faxincomingmessage_copytiff_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1vc6.htm
ms.date: 12/05/2018
ms.keywords: CopyTiff, CopyTiff method [Fax Service], CopyTiff method [Fax Service],IFaxIncomingMessage interface, IFaxIncomingMessage interface [Fax Service],CopyTiff method, IFaxIncomingMessage.CopyTiff, IFaxIncomingMessage::CopyTiff, _mfax_faxincomingmessage.copytiff, fax._mfax_faxincomingmessage_copytiff, fax._mfax_faxincomingmessage_cpp_mfax_faxincomingmessage_copytiff_cpp, faxcomex/IFaxIncomingMessage::CopyTiff
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
 - IFaxIncomingMessage::CopyTiff
 - faxcomex/IFaxIncomingMessage::CopyTiff
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
 - IFaxIncomingMessage.CopyTiff
---

# IFaxIncomingMessage::CopyTiff


## -description

The <b>CopyTiff</b> method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the inbound fax message to a file on the local computer.

## -parameters

### -param bstrTiffPath [in]

Type: <b>BSTR</b>

Null-terminated <b>BSTR</b> that specifies a fully qualified path and file name on the local computer. The fax service will copy the TIFF Class F file associated with the inbound fax message to the specified file.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessage">IFaxIncomingMessage</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-the-incoming-archive">Visual Basic Example</a>