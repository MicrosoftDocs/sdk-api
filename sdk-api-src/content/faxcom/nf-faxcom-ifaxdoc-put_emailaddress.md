---
UID: NF:faxcom.IFaxDoc.put_EmailAddress
title: IFaxDoc::put_EmailAddress (faxcom.h)
description: Sets or retrieves the EmailAddress property of a FaxDoc object. The EmailAddress property is a null-terminated string that contains the email address of the sender of the fax transmission. (Put)
helpviewer_keywords: ["EmailAddress property [Fax Service]","EmailAddress property [Fax Service]","IFaxDoc interface","IFaxDoc interface [Fax Service]","EmailAddress property","IFaxDoc.EmailAddress","IFaxDoc.put_EmailAddress","IFaxDoc::EmailAddress","IFaxDoc::get_EmailAddress","IFaxDoc::put_EmailAddress","_mfax_ifaxdoc_get_emailaddress","fax._mfax_ifaxdoc_get_emailaddress","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_emailaddress_cpp","faxcom/IFaxDoc::EmailAddress","faxcom/IFaxDoc::get_EmailAddress","faxcom/IFaxDoc::put_EmailAddress","put_EmailAddress"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_emailaddress_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7mwj.htm
ms.date: 12/05/2018
ms.keywords: EmailAddress property [Fax Service], EmailAddress property [Fax Service],IFaxDoc interface, IFaxDoc interface [Fax Service],EmailAddress property, IFaxDoc.EmailAddress, IFaxDoc.put_EmailAddress, IFaxDoc::EmailAddress, IFaxDoc::get_EmailAddress, IFaxDoc::put_EmailAddress, _mfax_ifaxdoc_get_emailaddress, fax._mfax_ifaxdoc_get_emailaddress, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_emailaddress_cpp, faxcom/IFaxDoc::EmailAddress, faxcom/IFaxDoc::get_EmailAddress, faxcom/IFaxDoc::put_EmailAddress, put_EmailAddress
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
 - IFaxDoc::put_EmailAddress
 - faxcom/IFaxDoc::put_EmailAddress
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
 - IFaxDoc.EmailAddress
 - IFaxDoc.get_EmailAddress
 - IFaxDoc.put_EmailAddress
---

# IFaxDoc::put_EmailAddress


## -description

Sets or retrieves the <b>EmailAddress</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>EmailAddress</b> property is a null-terminated string that contains the email address of the sender of the fax transmission.

This property is read/write.

## -parameters

## -remarks

The fax server uses the <b>EmailAddress</b> property to send delivery reports (DRs) and nondelivery reports (NDRs) to the sender of the transmission. The email address must be a valid address or alias in the Microsoft Exchange Server global address list (GAL).

The <b>get_EmailAddress</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
