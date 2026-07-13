---
UID: NF:faxcom.IFaxDoc.get_RecipientDepartment
title: IFaxDoc::get_RecipientDepartment (faxcom.h)
description: Sets or retrieves the RecipientDepartment property of a FaxDoc object. The RecipientDepartment property is a null-terminated string that contains the department of the recipient of the fax transmission. (Get)
helpviewer_keywords: ["IFaxDoc interface [Fax Service]","RecipientDepartment property","IFaxDoc.RecipientDepartment","IFaxDoc.get_RecipientDepartment","IFaxDoc::RecipientDepartment","IFaxDoc::get_RecipientDepartment","IFaxDoc::put_RecipientDepartment","RecipientDepartment property [Fax Service]","RecipientDepartment property [Fax Service]","IFaxDoc interface","_mfax_ifaxdoc_get_recipientdepartment","fax._mfax_ifaxdoc_get_recipientdepartment","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipientdepartment_cpp","faxcom/IFaxDoc::RecipientDepartment","faxcom/IFaxDoc::get_RecipientDepartment","faxcom/IFaxDoc::put_RecipientDepartment","get_RecipientDepartment"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_recipientdepartment_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3mk4.htm
ms.date: 12/05/2018
ms.keywords: IFaxDoc interface [Fax Service],RecipientDepartment property, IFaxDoc.RecipientDepartment, IFaxDoc.get_RecipientDepartment, IFaxDoc::RecipientDepartment, IFaxDoc::get_RecipientDepartment, IFaxDoc::put_RecipientDepartment, RecipientDepartment property [Fax Service], RecipientDepartment property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_recipientdepartment, fax._mfax_ifaxdoc_get_recipientdepartment, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipientdepartment_cpp, faxcom/IFaxDoc::RecipientDepartment, faxcom/IFaxDoc::get_RecipientDepartment, faxcom/IFaxDoc::put_RecipientDepartment, get_RecipientDepartment
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
 - IFaxDoc::get_RecipientDepartment
 - faxcom/IFaxDoc::get_RecipientDepartment
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
 - IFaxDoc.RecipientDepartment
 - IFaxDoc.get_RecipientDepartment
 - IFaxDoc.put_RecipientDepartment
---

# IFaxDoc::get_RecipientDepartment


## -description

Sets or retrieves the <b>RecipientDepartment</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>RecipientDepartment</b> property is a null-terminated string that contains the department of the recipient of the fax transmission.

This property is read/write.

## -parameters

## -remarks

The sender's fax number can appear on the cover page.

The <b>get_RecipientDepartment</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
