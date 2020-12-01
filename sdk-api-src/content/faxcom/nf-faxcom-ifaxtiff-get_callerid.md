---
UID: NF:faxcom.IFaxTiff.get_CallerId
title: IFaxTiff::get_CallerId (faxcom.h)
description: Retrieves the CallerId property for a FaxTiff object. The CallerId property is a string that identifies the calling device that sent a specified fax file.
helpviewer_keywords: ["CallerId property [Fax Service]","CallerId property [Fax Service]","IFaxTiff interface","IFaxTiff interface [Fax Service]","CallerId property","IFaxTiff.CallerId","IFaxTiff.get_CallerId","IFaxTiff::CallerId","IFaxTiff::get_CallerId","_mfax_ifaxtiff_get_callerid","fax._mfax_ifaxtiff_get_callerid","fax._mfax_ifaxtiff_mfax_ifaxtiff_get_callerid_cpp","faxcom/IFaxTiff::CallerId","faxcom/IFaxTiff::get_CallerId","get_CallerId"]
old-location: fax\_mfax_ifaxtiff_mfax_ifaxtiff_get_callerid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_502s.htm
ms.date: 12/05/2018
ms.keywords: CallerId property [Fax Service], CallerId property [Fax Service],IFaxTiff interface, IFaxTiff interface [Fax Service],CallerId property, IFaxTiff.CallerId, IFaxTiff.get_CallerId, IFaxTiff::CallerId, IFaxTiff::get_CallerId, _mfax_ifaxtiff_get_callerid, fax._mfax_ifaxtiff_get_callerid, fax._mfax_ifaxtiff_mfax_ifaxtiff_get_callerid_cpp, faxcom/IFaxTiff::CallerId, faxcom/IFaxTiff::get_CallerId, get_CallerId
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
 - IFaxTiff::get_CallerId
 - faxcom/IFaxTiff::get_CallerId
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
 - IFaxTiff.CallerId
 - IFaxTiff.get_CallerId
---

# IFaxTiff::get_CallerId


## -description

Retrieves the <b>CallerId</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object. The <b>CallerId</b> property is a string that identifies the calling device that sent a specified fax file.

This property is read-only.

## -parameters

## -remarks

A fax client application must  set the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-image-vb">Image</a> property before retrieving another property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object.

The <b>get_CallerId</b> method sets the <i>pVal</i> parameter to the string that identifies the calling device, if it is available. If the information is not available, the method returns "Unavailable".

The <b>CallerId</b> property is a string that identifies the calling device, if it is available. If the information is not available, <b>CallerId</b> is an empty string.

The <b>get_CallerId</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxtiff">IFaxTiff</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-image-vb">IFaxTiff::get_Image</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>