---
UID: NF:faxcom.IFaxStatus.get_CurrentPage
title: IFaxStatus::get_CurrentPage (faxcom.h)
description: Retrieves the CurrentPage property for the FaxStatus object of a parent FaxPort object. The CurrentPage property is a number that identifies the current page of an active outbound fax job on a specific port.
helpviewer_keywords: ["CurrentPage property [Fax Service]","CurrentPage property [Fax Service]","IFaxStatus interface","IFaxStatus interface [Fax Service]","CurrentPage property","IFaxStatus.CurrentPage","IFaxStatus.get_CurrentPage","IFaxStatus::CurrentPage","IFaxStatus::get_CurrentPage","_mfax_ifaxstatus_get_currentpage","fax._mfax_ifaxstatus_get_currentpage","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_currentpage_cpp","faxcom/IFaxStatus::CurrentPage","faxcom/IFaxStatus::get_CurrentPage","get_CurrentPage"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_currentpage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3kx1.htm
ms.date: 12/05/2018
ms.keywords: CurrentPage property [Fax Service], CurrentPage property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],CurrentPage property, IFaxStatus.CurrentPage, IFaxStatus.get_CurrentPage, IFaxStatus::CurrentPage, IFaxStatus::get_CurrentPage, _mfax_ifaxstatus_get_currentpage, fax._mfax_ifaxstatus_get_currentpage, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_currentpage_cpp, faxcom/IFaxStatus::CurrentPage, faxcom/IFaxStatus::get_CurrentPage, get_CurrentPage
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
 - IFaxStatus::get_CurrentPage
 - faxcom/IFaxStatus::get_CurrentPage
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
 - IFaxStatus.CurrentPage
 - IFaxStatus.get_CurrentPage
---

# IFaxStatus::get_CurrentPage


## -description

Retrieves the <b>CurrentPage</b> property for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>CurrentPage</b> property is a number that identifies the current page of an active outbound fax job on a specific port.

This property is read-only.

## -parameters

## -remarks

If the current page is not available, the <b>IFaxStatus::get_CurrentPage</b> method returns zero.

You can use the <b>CurrentPage</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object in conjunction with the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-pagecount-vb">PageCount</a> property of the object to provide users with a running page count for an outbound fax job. For example, you could inform a user that the fax server is currently transmitting the second page of a four page transmission.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-pagecount-vb">IFaxStatus::get_PageCount</a>