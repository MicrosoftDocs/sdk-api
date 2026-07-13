---
UID: NF:faxcom.IFaxDoc.put_RecipientTitle
title: IFaxDoc::put_RecipientTitle (faxcom.h)
description: Sets or retrieves the RecipientTitle property of a FaxDoc object. The RecipientTitle property is a null-terminated string that contains the title of the recipient of the fax transmission. (Put)
helpviewer_keywords: ["IFaxDoc interface [Fax Service]","RecipientTitle property","IFaxDoc.RecipientTitle","IFaxDoc.put_RecipientTitle","IFaxDoc::RecipientTitle","IFaxDoc::get_RecipientTitle","IFaxDoc::put_RecipientTitle","RecipientTitle property [Fax Service]","RecipientTitle property [Fax Service]","IFaxDoc interface","_mfax_ifaxdoc_get_recipienttitle","fax._mfax_ifaxdoc_get_recipienttitle","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipienttitle_cpp","faxcom/IFaxDoc::RecipientTitle","faxcom/IFaxDoc::get_RecipientTitle","faxcom/IFaxDoc::put_RecipientTitle","put_RecipientTitle"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_recipienttitle_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3bs5.htm
ms.date: 12/05/2018
ms.keywords: IFaxDoc interface [Fax Service],RecipientTitle property, IFaxDoc.RecipientTitle, IFaxDoc.put_RecipientTitle, IFaxDoc::RecipientTitle, IFaxDoc::get_RecipientTitle, IFaxDoc::put_RecipientTitle, RecipientTitle property [Fax Service], RecipientTitle property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_recipienttitle, fax._mfax_ifaxdoc_get_recipienttitle, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipienttitle_cpp, faxcom/IFaxDoc::RecipientTitle, faxcom/IFaxDoc::get_RecipientTitle, faxcom/IFaxDoc::put_RecipientTitle, put_RecipientTitle
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
 - IFaxDoc::put_RecipientTitle
 - faxcom/IFaxDoc::put_RecipientTitle
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
 - IFaxDoc.RecipientTitle
 - IFaxDoc.get_RecipientTitle
 - IFaxDoc.put_RecipientTitle
---

# IFaxDoc::put_RecipientTitle


## -description

Sets or retrieves the <b>RecipientTitle</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>RecipientTitle</b> property is a null-terminated string that contains the title of the recipient of the fax transmission.

This property is read/write.

## -parameters

## -remarks

The sender's fax number can appear on the cover page.

The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-senderfax-vb">get_SenderFax</a> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
