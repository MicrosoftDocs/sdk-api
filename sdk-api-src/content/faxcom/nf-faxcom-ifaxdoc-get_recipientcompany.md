---
UID: NF:faxcom.IFaxDoc.get_RecipientCompany
title: IFaxDoc::get_RecipientCompany (faxcom.h)
description: Sets or retrieves the RecipientCompany property of a FaxDoc object. The RecipientCompany property is a null-terminated string that contains the company name of the recipient of the fax transmission. (Get)
helpviewer_keywords: ["IFaxDoc interface [Fax Service]","RecipientCompany property","IFaxDoc.RecipientCompany","IFaxDoc.get_RecipientCompany","IFaxDoc::RecipientCompany","IFaxDoc::get_RecipientCompany","IFaxDoc::put_RecipientCompany","RecipientCompany property [Fax Service]","RecipientCompany property [Fax Service]","IFaxDoc interface","_mfax_ifaxdoc_get_recipientcompany","fax._mfax_ifaxdoc_get_recipientcompany","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipientcompany_cpp","faxcom/IFaxDoc::RecipientCompany","faxcom/IFaxDoc::get_RecipientCompany","faxcom/IFaxDoc::put_RecipientCompany","get_RecipientCompany"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_recipientcompany_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0rjt.htm
ms.date: 12/05/2018
ms.keywords: IFaxDoc interface [Fax Service],RecipientCompany property, IFaxDoc.RecipientCompany, IFaxDoc.get_RecipientCompany, IFaxDoc::RecipientCompany, IFaxDoc::get_RecipientCompany, IFaxDoc::put_RecipientCompany, RecipientCompany property [Fax Service], RecipientCompany property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_recipientcompany, fax._mfax_ifaxdoc_get_recipientcompany, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipientcompany_cpp, faxcom/IFaxDoc::RecipientCompany, faxcom/IFaxDoc::get_RecipientCompany, faxcom/IFaxDoc::put_RecipientCompany, get_RecipientCompany
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
 - IFaxDoc::get_RecipientCompany
 - faxcom/IFaxDoc::get_RecipientCompany
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
 - IFaxDoc.RecipientCompany
 - IFaxDoc.get_RecipientCompany
 - IFaxDoc.put_RecipientCompany
---

# IFaxDoc::get_RecipientCompany


## -description

Sets or retrieves the <b>RecipientCompany</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>RecipientCompany</b> property is a null-terminated string that contains the company name of the recipient of the fax transmission.

This property is read/write.

## -parameters

## -remarks

The fax recipient's company name can appear on the cover page.

The <b>get_RecipientCompany</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
