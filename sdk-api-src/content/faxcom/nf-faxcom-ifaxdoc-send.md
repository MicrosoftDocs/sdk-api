---
UID: NF:faxcom.IFaxDoc.Send
title: IFaxDoc::Send (faxcom.h)
description: The Send method transmits the document specified by the FileName property of a FaxDoc object. The method can send the fax to the fax number specified by the FaxNumber property.
helpviewer_keywords: ["IFaxDoc interface [Fax Service]","Send method","IFaxDoc.Send","IFaxDoc::Send","Send","Send method [Fax Service]","Send method [Fax Service]","IFaxDoc interface","_mfax_ifaxdoc_send","fax._mfax_ifaxdoc_mfax_ifaxdoc_send_cpp","fax._mfax_ifaxdoc_send","faxcom/IFaxDoc::Send"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_send_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8o2s.htm
ms.date: 12/05/2018
ms.keywords: IFaxDoc interface [Fax Service],Send method, IFaxDoc.Send, IFaxDoc::Send, Send, Send method [Fax Service], Send method [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_send, fax._mfax_ifaxdoc_mfax_ifaxdoc_send_cpp, fax._mfax_ifaxdoc_send, faxcom/IFaxDoc::Send
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Faxcom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxDoc::Send
 - faxcom/IFaxDoc::Send
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxDoc.Send
 - IFaxDoc.Send
---

# IFaxDoc::Send


## -description

The <b>Send</b> method transmits the document specified by the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-filename-vb">FileName</a> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The method can send the fax to the fax number specified by the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-faxnumber-vb">FaxNumber</a> property.

## -parameters

### -param pVal [out, retval]

Type: <b>LONG*</b>

Specifies a pointer to a variable to receive a unique number that identifies the queued job that will send the fax transmission.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-filename-vb">FileName</a> property is required to send a fax transmission using a call to the <b>IFaxDoc::Send</b> method. The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-faxnumber-vb">FaxNumber</a> property is also required. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-transmitting-faxes">Transmitting Faxes</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>