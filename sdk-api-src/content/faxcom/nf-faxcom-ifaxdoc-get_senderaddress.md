---
UID: NF:faxcom.IFaxDoc.get_SenderAddress
title: IFaxDoc::get_SenderAddress (faxcom.h)
author: windows-sdk-content
description: Sets or retrieves the SenderAddress property of a FaxDoc object. The SenderAddress property is a null-terminated string that contains the street address of the sender of the fax transmission.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_senderaddress_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_58vn.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxDoc interface [Fax Service],SenderAddress property, IFaxDoc.SenderAddress, IFaxDoc.get_SenderAddress, IFaxDoc::SenderAddress, IFaxDoc::get_SenderAddress, IFaxDoc::put_SenderAddress, SenderAddress property [Fax Service], SenderAddress property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_senderaddress, fax._mfax_ifaxdoc_get_senderaddress, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_senderaddress_cpp, faxcom/IFaxDoc::SenderAddress, faxcom/IFaxDoc::get_SenderAddress, faxcom/IFaxDoc::put_SenderAddress, get_SenderAddress
ms.topic: method
f1_keywords: 
 - "faxcom/IFaxDoc.SenderAddress"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxDoc.SenderAddress
 - IFaxDoc.get_SenderAddress
 - IFaxDoc.put_SenderAddress
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxDoc::get_SenderAddress


## -description


Sets or retrieves the <b>SenderAddress</b> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>SenderAddress</b> property is a null-terminated string that contains the street address of the sender of the fax transmission.

This property is read/write.


## -parameters


## -remarks



The fax sender's street address can appear on the cover page.

The <b>get_SenderAddress</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
 

 

