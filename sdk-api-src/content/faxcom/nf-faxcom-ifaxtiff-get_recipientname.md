---
UID: NF:faxcom.IFaxTiff.get_RecipientName
title: IFaxTiff::get_RecipientName (faxcom.h)
description: Retrieves the RecipientName property for a FaxTiff object. The RecipientName property is a null-terminated string that contains the name of the recipient for the specified fax file.
helpviewer_keywords: ["IFaxTiff interface [Fax Service]","RecipientName property","IFaxTiff.RecipientName","IFaxTiff.get_RecipientName","IFaxTiff::RecipientName","IFaxTiff::get_RecipientName","RecipientName property [Fax Service]","RecipientName property [Fax Service]","IFaxTiff interface","_mfax_ifaxtiff_get_recipientname","fax._mfax_ifaxtiff_get_recipientname","fax._mfax_ifaxtiff_mfax_ifaxtiff_get_recipientname_cpp","faxcom/IFaxTiff::RecipientName","faxcom/IFaxTiff::get_RecipientName","get_RecipientName"]
old-location: fax\_mfax_ifaxtiff_mfax_ifaxtiff_get_recipientname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_29b9.htm
ms.date: 12/05/2018
ms.keywords: IFaxTiff interface [Fax Service],RecipientName property, IFaxTiff.RecipientName, IFaxTiff.get_RecipientName, IFaxTiff::RecipientName, IFaxTiff::get_RecipientName, RecipientName property [Fax Service], RecipientName property [Fax Service],IFaxTiff interface, _mfax_ifaxtiff_get_recipientname, fax._mfax_ifaxtiff_get_recipientname, fax._mfax_ifaxtiff_mfax_ifaxtiff_get_recipientname_cpp, faxcom/IFaxTiff::RecipientName, faxcom/IFaxTiff::get_RecipientName, get_RecipientName
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
 - IFaxTiff::get_RecipientName
 - faxcom/IFaxTiff::get_RecipientName
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
 - IFaxTiff.RecipientName
 - IFaxTiff.get_RecipientName
---

# IFaxTiff::get_RecipientName


## -description

Retrieves the <b>RecipientName</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object. The <b>RecipientName</b> property is a null-terminated string that contains the name of the recipient for the specified fax file.

This property is read-only.

## -parameters

## -remarks

A fax client application must  set the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-image-vb">Image</a> property before retrieving another property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object.

The <b>get_RecipientName</b> method sets the <i>pVal</i> parameter to the name of the fax recipient, if it is available. If the information is not available, the method returns "Unavailable".

The <b>RecipientName</b> property is a string that represents the name of the fax recipient, if it is available. If the information is not available, <b>RecipientName</b> is an empty string.

The <b>get_RecipientName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxtiff">IFaxTiff</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-image-vb">IFaxTiff::get_Image</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>