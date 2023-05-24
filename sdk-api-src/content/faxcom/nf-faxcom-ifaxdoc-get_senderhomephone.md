---
UID: NF:faxcom.IFaxDoc.get_SenderHomePhone
title: IFaxDoc::get_SenderHomePhone (faxcom.h)
description: Sets or retrieves the SenderHomePhone property of a FaxDoc object. The SenderHomePhone property is a null-terminated string that contains the home telephone number of the sender of the fax transmission. (Get)
helpviewer_keywords: ["IFaxDoc interface [Fax Service]","SenderHomePhone property","IFaxDoc.SenderHomePhone","IFaxDoc.get_SenderHomePhone","IFaxDoc::SenderHomePhone","IFaxDoc::get_SenderHomePhone","IFaxDoc::put_SenderHomePhone","SenderHomePhone property [Fax Service]","SenderHomePhone property [Fax Service]","IFaxDoc interface","_mfax_ifaxdoc_get_senderhomephone","fax._mfax_ifaxdoc_get_senderhomephone","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_senderhomephone_cpp","faxcom/IFaxDoc::SenderHomePhone","faxcom/IFaxDoc::get_SenderHomePhone","faxcom/IFaxDoc::put_SenderHomePhone","get_SenderHomePhone"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_senderhomephone_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_93l1.htm
ms.date: 12/05/2018
ms.keywords: IFaxDoc interface [Fax Service],SenderHomePhone property, IFaxDoc.SenderHomePhone, IFaxDoc.get_SenderHomePhone, IFaxDoc::SenderHomePhone, IFaxDoc::get_SenderHomePhone, IFaxDoc::put_SenderHomePhone, SenderHomePhone property [Fax Service], SenderHomePhone property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_senderhomephone, fax._mfax_ifaxdoc_get_senderhomephone, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_senderhomephone_cpp, faxcom/IFaxDoc::SenderHomePhone, faxcom/IFaxDoc::get_SenderHomePhone, faxcom/IFaxDoc::put_SenderHomePhone, get_SenderHomePhone
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
 - IFaxDoc::get_SenderHomePhone
 - faxcom/IFaxDoc::get_SenderHomePhone
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
 - IFaxDoc.SenderHomePhone
 - IFaxDoc.get_SenderHomePhone
 - IFaxDoc.put_SenderHomePhone
---

# IFaxDoc::get_SenderHomePhone


## -description

Sets or retrieves the <b>SenderHomePhone</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>SenderHomePhone</b> property is a null-terminated string that contains the home telephone number of the sender of the fax transmission.

This property is read/write.

## -parameters

## -remarks

The fax sender's home telephone number can appear on the cover page.

The <b>get_SenderHomePhone</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
