---
UID: NF:faxcom.IFaxDoc.put_BillingCode
title: IFaxDoc::put_BillingCode (faxcom.h)
description: Sets or retrieves the BillingCode property of a FaxDoc object. The BillingCode property is a null-terminated string that contains an optional billing code that applies to the fax transmission. (Put)
helpviewer_keywords: ["BillingCode property [Fax Service]","BillingCode property [Fax Service]","IFaxDoc interface","IFaxDoc interface [Fax Service]","BillingCode property","IFaxDoc.BillingCode","IFaxDoc.put_BillingCode","IFaxDoc::BillingCode","IFaxDoc::get_BillingCode","IFaxDoc::put_BillingCode","_mfax_ifaxdoc_get_billingcode","fax._mfax_ifaxdoc_get_billingcode","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_billingcode_cpp","faxcom/IFaxDoc::BillingCode","faxcom/IFaxDoc::get_BillingCode","faxcom/IFaxDoc::put_BillingCode","put_BillingCode"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_billingcode_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_95yd.htm
ms.date: 12/05/2018
ms.keywords: BillingCode property [Fax Service], BillingCode property [Fax Service],IFaxDoc interface, IFaxDoc interface [Fax Service],BillingCode property, IFaxDoc.BillingCode, IFaxDoc.put_BillingCode, IFaxDoc::BillingCode, IFaxDoc::get_BillingCode, IFaxDoc::put_BillingCode, _mfax_ifaxdoc_get_billingcode, fax._mfax_ifaxdoc_get_billingcode, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_billingcode_cpp, faxcom/IFaxDoc::BillingCode, faxcom/IFaxDoc::get_BillingCode, faxcom/IFaxDoc::put_BillingCode, put_BillingCode
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
 - IFaxDoc::put_BillingCode
 - faxcom/IFaxDoc::put_BillingCode
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
 - IFaxDoc.BillingCode
 - IFaxDoc.get_BillingCode
 - IFaxDoc.put_BillingCode
---

# IFaxDoc::put_BillingCode


## -description

Sets or retrieves the <b>BillingCode</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>BillingCode</b> property is a null-terminated string that contains an optional billing code that applies to the fax transmission.

This property is read/write.

## -parameters

## -remarks

The fax server uses the <b>BillingCode</b> property to generate an entry in the fax event log. Billing codes are optional.

The <b>get_BillingCode</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
