---
UID: NF:faxcom.IFaxStatus.get_PageCount
title: IFaxStatus::get_PageCount (faxcom.h)
description: Retrieves the PageCount property for the FaxStatus object of a parent FaxPort object. The PageCount property represents the total number of pages in an outbound fax transmission.
helpviewer_keywords: ["IFaxStatus interface [Fax Service]","PageCount property","IFaxStatus.PageCount","IFaxStatus.get_PageCount","IFaxStatus::PageCount","IFaxStatus::get_PageCount","PageCount property [Fax Service]","PageCount property [Fax Service]","IFaxStatus interface","_mfax_ifaxstatus_get_pagecount","fax._mfax_ifaxstatus_get_pagecount","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_pagecount_cpp","faxcom/IFaxStatus::PageCount","faxcom/IFaxStatus::get_PageCount","get_PageCount"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_pagecount_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6xv8.htm
ms.date: 12/05/2018
ms.keywords: IFaxStatus interface [Fax Service],PageCount property, IFaxStatus.PageCount, IFaxStatus.get_PageCount, IFaxStatus::PageCount, IFaxStatus::get_PageCount, PageCount property [Fax Service], PageCount property [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_get_pagecount, fax._mfax_ifaxstatus_get_pagecount, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_pagecount_cpp, faxcom/IFaxStatus::PageCount, faxcom/IFaxStatus::get_PageCount, get_PageCount
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
 - IFaxStatus::get_PageCount
 - faxcom/IFaxStatus::get_PageCount
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
 - IFaxStatus.PageCount
 - IFaxStatus.get_PageCount
---

# IFaxStatus::get_PageCount


## -description

Retrieves the <b>PageCount</b> property for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>PageCount</b> property represents the total number of pages in an outbound fax transmission.

This property is read-only.

## -parameters

## -remarks

If the page count is not available, the <b>IFaxStatus::get_PageCount</b> method returns zero.

You can use the <b>PageCount</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object in conjunction with the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-currentpage-vb">CurrentPage</a> property of the object to provide users with a running page count for an outbound fax job. For example, you could inform a user that the fax server is currently transmitting the second page of a four page transmission.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-currentpage-vb">IFaxStatus::get_CurrentPage</a>