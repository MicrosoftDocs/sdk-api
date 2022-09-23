---
UID: NF:faxcom.IFaxDoc.put_SenderOfficePhone
title: IFaxDoc::put_SenderOfficePhone (faxcom.h)
description: Sets or retrieves the SenderOfficePhone property of a FaxDoc object. The SenderOfficePhone property is a null-terminated string that contains the office telephone number of the sender of the fax transmission. (Put)
helpviewer_keywords: ["IFaxDoc interface [Fax Service]","SenderOfficePhone property","IFaxDoc.SenderOfficePhone","IFaxDoc.put_SenderOfficePhone","IFaxDoc::SenderOfficePhone","IFaxDoc::get_SenderOfficePhone","IFaxDoc::put_SenderOfficePhone","SenderOfficePhone property [Fax Service]","SenderOfficePhone property [Fax Service]","IFaxDoc interface","_mfax_ifaxdoc_get_senderofficephone","fax._mfax_ifaxdoc_get_senderofficephone","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_senderofficephone_cpp","faxcom/IFaxDoc::SenderOfficePhone","faxcom/IFaxDoc::get_SenderOfficePhone","faxcom/IFaxDoc::put_SenderOfficePhone","put_SenderOfficePhone"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_senderofficephone_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0mzp.htm
ms.date: 12/05/2018
ms.keywords: IFaxDoc interface [Fax Service],SenderOfficePhone property, IFaxDoc.SenderOfficePhone, IFaxDoc.put_SenderOfficePhone, IFaxDoc::SenderOfficePhone, IFaxDoc::get_SenderOfficePhone, IFaxDoc::put_SenderOfficePhone, SenderOfficePhone property [Fax Service], SenderOfficePhone property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_senderofficephone, fax._mfax_ifaxdoc_get_senderofficephone, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_senderofficephone_cpp, faxcom/IFaxDoc::SenderOfficePhone, faxcom/IFaxDoc::get_SenderOfficePhone, faxcom/IFaxDoc::put_SenderOfficePhone, put_SenderOfficePhone
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
 - IFaxDoc::put_SenderOfficePhone
 - faxcom/IFaxDoc::put_SenderOfficePhone
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
 - IFaxDoc.SenderOfficePhone
 - IFaxDoc.get_SenderOfficePhone
 - IFaxDoc.put_SenderOfficePhone
---

# IFaxDoc::put_SenderOfficePhone


## -description

Sets or retrieves the <b>SenderOfficePhone</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>SenderOfficePhone</b> property is a null-terminated string that contains the office telephone number of the sender of the fax transmission.

This property is read/write.

## -parameters

## -remarks

The fax sender's office telephone number can appear on the cover page.

The <b>IFaxDoc::get_SenderOfficePhone</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
