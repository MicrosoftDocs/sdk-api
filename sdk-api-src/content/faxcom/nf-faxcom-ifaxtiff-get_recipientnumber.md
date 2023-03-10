---
UID: NF:faxcom.IFaxTiff.get_RecipientNumber
title: IFaxTiff::get_RecipientNumber (faxcom.h)
description: Retrieves the RecipientNumber property for a FaxTiff object. The RecipientNumber property is a null-terminated string that contains the fax number to which a fax was transmitted.
helpviewer_keywords: ["IFaxTiff interface [Fax Service]","RecipientNumber property","IFaxTiff.RecipientNumber","IFaxTiff.get_RecipientNumber","IFaxTiff::RecipientNumber","IFaxTiff::get_RecipientNumber","RecipientNumber property [Fax Service]","RecipientNumber property [Fax Service]","IFaxTiff interface","_mfax_ifaxtiff_get_recipientnumber","fax._mfax_ifaxtiff_get_recipientnumber","fax._mfax_ifaxtiff_mfax_ifaxtiff_get_recipientnumber_cpp","faxcom/IFaxTiff::RecipientNumber","faxcom/IFaxTiff::get_RecipientNumber","get_RecipientNumber"]
old-location: fax\_mfax_ifaxtiff_mfax_ifaxtiff_get_recipientnumber_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3b8y.htm
ms.date: 12/05/2018
ms.keywords: IFaxTiff interface [Fax Service],RecipientNumber property, IFaxTiff.RecipientNumber, IFaxTiff.get_RecipientNumber, IFaxTiff::RecipientNumber, IFaxTiff::get_RecipientNumber, RecipientNumber property [Fax Service], RecipientNumber property [Fax Service],IFaxTiff interface, _mfax_ifaxtiff_get_recipientnumber, fax._mfax_ifaxtiff_get_recipientnumber, fax._mfax_ifaxtiff_mfax_ifaxtiff_get_recipientnumber_cpp, faxcom/IFaxTiff::RecipientNumber, faxcom/IFaxTiff::get_RecipientNumber, get_RecipientNumber
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
 - IFaxTiff::get_RecipientNumber
 - faxcom/IFaxTiff::get_RecipientNumber
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
 - IFaxTiff.RecipientNumber
 - IFaxTiff.get_RecipientNumber
---

# IFaxTiff::get_RecipientNumber


## -description

Retrieves the <b>RecipientNumber</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object. The <b>RecipientNumber</b> property is a null-terminated string that contains the fax number to which a fax was transmitted.

This property is read-only.

## -parameters

## -remarks

A fax client application must  set the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-image-vb">Image</a> property before retrieving another property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object.

The <b>RecipientNumber</b> property has meaning only for outbound fax transmissions. This is because the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-csid-vb">Csid</a> property and the <b>RecipientNumber</b> property are identical for inbound faxes.

The <b>get_RecipientNumber</b> method sets the <i>pVal</i> parameter to the fax number of the fax recipient, if it is available. If the information is not available, the method returns "Unavailable".

The <b>RecipientNumber</b> property is a string that represents the fax number of the fax recipient, if it is available. If the information is not available, <b>RecipientNumber</b> is an empty string.

The <b>get_RecipientNumber</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxtiff">IFaxTiff</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-csid-vb">IFaxTiff::get_Csid</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-image-vb">IFaxTiff::get_Image</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>