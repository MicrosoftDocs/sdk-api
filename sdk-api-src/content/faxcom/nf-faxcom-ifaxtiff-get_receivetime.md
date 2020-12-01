---
UID: NF:faxcom.IFaxTiff.get_ReceiveTime
title: IFaxTiff::get_ReceiveTime (faxcom.h)
description: Retrieves the ReceiveTime property for a FaxTiff object.
helpviewer_keywords: ["IFaxTiff interface [Fax Service]","ReceiveTime property","IFaxTiff.ReceiveTime","IFaxTiff.get_ReceiveTime","IFaxTiff::ReceiveTime","IFaxTiff::get_ReceiveTime","ReceiveTime property [Fax Service]","ReceiveTime property [Fax Service]","IFaxTiff interface","_mfax_ifaxtiff_get_receivetime","fax._mfax_ifaxtiff_get_receivetime","fax._mfax_ifaxtiff_mfax_ifaxtiff_get_receivetime_cpp","faxcom/IFaxTiff::ReceiveTime","faxcom/IFaxTiff::get_ReceiveTime","get_ReceiveTime"]
old-location: fax\_mfax_ifaxtiff_mfax_ifaxtiff_get_receivetime_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5spx.htm
ms.date: 12/05/2018
ms.keywords: IFaxTiff interface [Fax Service],ReceiveTime property, IFaxTiff.ReceiveTime, IFaxTiff.get_ReceiveTime, IFaxTiff::ReceiveTime, IFaxTiff::get_ReceiveTime, ReceiveTime property [Fax Service], ReceiveTime property [Fax Service],IFaxTiff interface, _mfax_ifaxtiff_get_receivetime, fax._mfax_ifaxtiff_get_receivetime, fax._mfax_ifaxtiff_mfax_ifaxtiff_get_receivetime_cpp, faxcom/IFaxTiff::ReceiveTime, faxcom/IFaxTiff::get_ReceiveTime, get_ReceiveTime
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
 - IFaxTiff::get_ReceiveTime
 - faxcom/IFaxTiff::get_ReceiveTime
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
 - IFaxTiff.ReceiveTime
 - IFaxTiff.get_ReceiveTime
---

# IFaxTiff::get_ReceiveTime


## -description

Retrieves the <b>ReceiveTime</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object. The <b>ReceiveTime</b> property is a null-terminated string that contains the time at which reception began for an inbound fax file. The string can contain the time at which reception or transmission began for an archived file.

This property is read-only.

## -parameters

## -remarks

A fax client application must  set the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-image-vb">Image</a> property before retrieving another property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object.

The <b>get_ReceiveTime</b> method sets the <i>pVal</i> parameter to the time at which reception began for an inbound fax file, if it is available. If the information is not available, the method returns an empty string.

The <b>ReceiveTime</b> property is a string that represents the time at which reception began for an inbound fax file, if it is available. If the information is not available, <b>RecipientName</b> is "Unavailable".

The <b>get_ReceiveTime</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

The fax service formats the string according to the user's locale. It is a concatenation of the date and time the service transmitted the fax. The date is separated from the time by an "@" character. For example, in the English locale, a string would be formatted as follows:

10/02/98@10:15AM

The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-rawreceivetime-vb">RawReceiveTime</a> property contains the time expressed in Coordinated Universal Time (UTC).

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxtiff">IFaxTiff</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-image-vb">IFaxTiff::get_Image</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-rawreceivetime-vb">IFaxTiff::get_RawReceiveTime</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>