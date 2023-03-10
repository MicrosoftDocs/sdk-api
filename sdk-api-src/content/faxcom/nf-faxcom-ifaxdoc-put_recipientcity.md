---
UID: NF:faxcom.IFaxDoc.put_RecipientCity
title: IFaxDoc::put_RecipientCity (faxcom.h)
description: Sets or retrieves the RecipientCity property of a FaxDoc object. The RecipientCity property is a null-terminated string that contains the city name of the recipient of the fax transmission. (Put)
helpviewer_keywords: ["IFaxDoc interface [Fax Service]","RecipientCity property","IFaxDoc.RecipientCity","IFaxDoc.put_RecipientCity","IFaxDoc::RecipientCity","IFaxDoc::get_RecipientCity","IFaxDoc::put_RecipientCity","RecipientCity property [Fax Service]","RecipientCity property [Fax Service]","IFaxDoc interface","_mfax_ifaxdoc_get_recipientcity","fax._mfax_ifaxdoc_get_recipientcity","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipientcity_cpp","faxcom/IFaxDoc::RecipientCity","faxcom/IFaxDoc::get_RecipientCity","faxcom/IFaxDoc::put_RecipientCity","put_RecipientCity"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_recipientcity_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_4uih.htm
ms.date: 12/05/2018
ms.keywords: IFaxDoc interface [Fax Service],RecipientCity property, IFaxDoc.RecipientCity, IFaxDoc.put_RecipientCity, IFaxDoc::RecipientCity, IFaxDoc::get_RecipientCity, IFaxDoc::put_RecipientCity, RecipientCity property [Fax Service], RecipientCity property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_recipientcity, fax._mfax_ifaxdoc_get_recipientcity, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipientcity_cpp, faxcom/IFaxDoc::RecipientCity, faxcom/IFaxDoc::get_RecipientCity, faxcom/IFaxDoc::put_RecipientCity, put_RecipientCity
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
 - IFaxDoc::put_RecipientCity
 - faxcom/IFaxDoc::put_RecipientCity
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
 - IFaxDoc.RecipientCity
 - IFaxDoc.get_RecipientCity
 - IFaxDoc.put_RecipientCity
---

# IFaxDoc::put_RecipientCity


## -description

Sets or retrieves the <b>RecipientCity</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>RecipientCity</b> property is a null-terminated string that contains the city name of the recipient of the fax transmission.

This property is read/write.

## -parameters

## -remarks

The fax recipient's city name can appear on the cover page.

The <b>get_RecipientCity</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
