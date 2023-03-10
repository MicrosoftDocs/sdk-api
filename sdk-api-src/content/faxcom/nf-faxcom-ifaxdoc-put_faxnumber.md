---
UID: NF:faxcom.IFaxDoc.put_FaxNumber
title: IFaxDoc::put_FaxNumber (faxcom.h)
description: Sets or retrieves the FaxNumber property of a FaxDoc object. The FaxNumber property is a null-terminated string that contains the fax number to which the fax server will send the fax transmission. (Put)
helpviewer_keywords: ["FaxNumber property [Fax Service]","FaxNumber property [Fax Service]","IFaxDoc interface","IFaxDoc interface [Fax Service]","FaxNumber property","IFaxDoc.FaxNumber","IFaxDoc.put_FaxNumber","IFaxDoc::FaxNumber","IFaxDoc::get_FaxNumber","IFaxDoc::put_FaxNumber","_mfax_ifaxdoc_get_faxnumber","fax._mfax_ifaxdoc_get_faxnumber","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_faxnumber_cpp","faxcom/IFaxDoc::FaxNumber","faxcom/IFaxDoc::get_FaxNumber","faxcom/IFaxDoc::put_FaxNumber","put_FaxNumber"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_faxnumber_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_833m.htm
ms.date: 12/05/2018
ms.keywords: FaxNumber property [Fax Service], FaxNumber property [Fax Service],IFaxDoc interface, IFaxDoc interface [Fax Service],FaxNumber property, IFaxDoc.FaxNumber, IFaxDoc.put_FaxNumber, IFaxDoc::FaxNumber, IFaxDoc::get_FaxNumber, IFaxDoc::put_FaxNumber, _mfax_ifaxdoc_get_faxnumber, fax._mfax_ifaxdoc_get_faxnumber, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_faxnumber_cpp, faxcom/IFaxDoc::FaxNumber, faxcom/IFaxDoc::get_FaxNumber, faxcom/IFaxDoc::put_FaxNumber, put_FaxNumber
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
 - IFaxDoc::put_FaxNumber
 - faxcom/IFaxDoc::put_FaxNumber
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
 - IFaxDoc.FaxNumber
 - IFaxDoc.get_FaxNumber
 - IFaxDoc.put_FaxNumber
---

# IFaxDoc::put_FaxNumber


## -description

Sets or retrieves the <b>FaxNumber</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>FaxNumber</b> property is a null-terminated string that contains the fax number to which the fax server will send the fax transmission.

This property is read/write.

## -parameters

## -remarks

The recipient's fax number can appear on the cover page. 

The <b>FaxNumber</b> property is required to send a fax transmission using a call to the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-send-vb">IFaxDoc::Send</a> method. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-transmitting-faxes">Transmitting Faxes</a>.

The <b>FaxNumber</b> property is required to send a fax transmission using a call to the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-send-vb">Send</a> method. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-transmitting-faxes">Transmitting Faxes</a>.

The <b>get_FaxNumber</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-send-vb">IFaxDoc::Send</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
