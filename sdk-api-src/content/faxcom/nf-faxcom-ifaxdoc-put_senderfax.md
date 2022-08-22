---
UID: NF:faxcom.IFaxDoc.put_SenderFax
title: IFaxDoc::put_SenderFax (faxcom.h)
description: Sets or retrieves the SenderFax property of a FaxDoc object. The SenderFax property is a null-terminated string that contains the fax number of the sender of the outbound fax transmission. (Put)
helpviewer_keywords: ["IFaxDoc interface [Fax Service]","SenderFax property","IFaxDoc.SenderFax","IFaxDoc.put_SenderFax","IFaxDoc::SenderFax","IFaxDoc::get_SenderFax","IFaxDoc::put_SenderFax","SenderFax property [Fax Service]","SenderFax property [Fax Service]","IFaxDoc interface","_mfax_ifaxdoc_get_senderfax","fax._mfax_ifaxdoc_get_senderfax","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_senderfax_cpp","faxcom/IFaxDoc::SenderFax","faxcom/IFaxDoc::get_SenderFax","faxcom/IFaxDoc::put_SenderFax","put_SenderFax"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_senderfax_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_02ew.htm
ms.date: 12/05/2018
ms.keywords: IFaxDoc interface [Fax Service],SenderFax property, IFaxDoc.SenderFax, IFaxDoc.put_SenderFax, IFaxDoc::SenderFax, IFaxDoc::get_SenderFax, IFaxDoc::put_SenderFax, SenderFax property [Fax Service], SenderFax property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_senderfax, fax._mfax_ifaxdoc_get_senderfax, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_senderfax_cpp, faxcom/IFaxDoc::SenderFax, faxcom/IFaxDoc::get_SenderFax, faxcom/IFaxDoc::put_SenderFax, put_SenderFax
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
 - IFaxDoc::put_SenderFax
 - faxcom/IFaxDoc::put_SenderFax
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
 - IFaxDoc.SenderFax
 - IFaxDoc.get_SenderFax
 - IFaxDoc.put_SenderFax
---

# IFaxDoc::put_SenderFax


## -description

Sets or retrieves the <b>SenderFax</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>SenderFax</b> property is a null-terminated string that contains the fax number of the sender of the outbound fax transmission.

This property is read/write.

## -parameters

## -remarks

The sender's fax number can appear on the cover page.

The <b>get_SenderFax</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
