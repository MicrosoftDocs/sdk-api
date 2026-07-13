---
UID: NF:faxcom.IFaxDoc.get_SenderTitle
title: IFaxDoc::get_SenderTitle (faxcom.h)
description: Sets or retrieves the SenderTitle property of a FaxDoc object. The SenderTitle property is a null-terminated string that contains the title of the sender of the fax transmission. (Get)
helpviewer_keywords: ["IFaxDoc interface [Fax Service]","SenderTitle property","IFaxDoc.SenderTitle","IFaxDoc.get_SenderTitle","IFaxDoc::SenderTitle","IFaxDoc::get_SenderTitle","IFaxDoc::put_SenderTitle","SenderTitle property [Fax Service]","SenderTitle property [Fax Service]","IFaxDoc interface","_mfax_ifaxdoc_get_sendertitle","fax._mfax_ifaxdoc_get_sendertitle","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_sendertitle_cpp","faxcom/IFaxDoc::SenderTitle","faxcom/IFaxDoc::get_SenderTitle","faxcom/IFaxDoc::put_SenderTitle","get_SenderTitle"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_sendertitle_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3obp.htm
ms.date: 12/05/2018
ms.keywords: IFaxDoc interface [Fax Service],SenderTitle property, IFaxDoc.SenderTitle, IFaxDoc.get_SenderTitle, IFaxDoc::SenderTitle, IFaxDoc::get_SenderTitle, IFaxDoc::put_SenderTitle, SenderTitle property [Fax Service], SenderTitle property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_sendertitle, fax._mfax_ifaxdoc_get_sendertitle, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_sendertitle_cpp, faxcom/IFaxDoc::SenderTitle, faxcom/IFaxDoc::get_SenderTitle, faxcom/IFaxDoc::put_SenderTitle, get_SenderTitle
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
 - IFaxDoc::get_SenderTitle
 - faxcom/IFaxDoc::get_SenderTitle
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
 - IFaxDoc.SenderTitle
 - IFaxDoc.get_SenderTitle
 - IFaxDoc.put_SenderTitle
---

# IFaxDoc::get_SenderTitle


## -description

Sets or retrieves the <b>SenderTitle</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>SenderTitle</b> property is a null-terminated string that contains the title of the sender of the fax transmission.

This property is read/write.

## -parameters

## -remarks

The fax sender's title can appear on the cover page.

The <b>get_SenderTitle</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
