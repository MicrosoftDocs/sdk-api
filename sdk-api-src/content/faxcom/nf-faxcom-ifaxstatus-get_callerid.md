---
UID: NF:faxcom.IFaxStatus.get_CallerId
title: IFaxStatus::get_CallerId (faxcom.h)
description: Retrieves the CallerId property for the FaxStatus object of a parent FaxPort object. The CallerId property is a string that identifies the calling device that sent an inbound fax job.
helpviewer_keywords: ["CallerId property [Fax Service]","CallerId property [Fax Service]","IFaxStatus interface","IFaxStatus interface [Fax Service]","CallerId property","IFaxStatus.CallerId","IFaxStatus.get_CallerId","IFaxStatus::CallerId","IFaxStatus::get_CallerId","_mfax_ifaxstatus_get_callerid","fax._mfax_ifaxstatus_get_callerid","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_callerid_cpp","faxcom/IFaxStatus::CallerId","faxcom/IFaxStatus::get_CallerId","get_CallerId"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_callerid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3kx0.htm
ms.date: 12/05/2018
ms.keywords: CallerId property [Fax Service], CallerId property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],CallerId property, IFaxStatus.CallerId, IFaxStatus.get_CallerId, IFaxStatus::CallerId, IFaxStatus::get_CallerId, _mfax_ifaxstatus_get_callerid, fax._mfax_ifaxstatus_get_callerid, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_callerid_cpp, faxcom/IFaxStatus::CallerId, faxcom/IFaxStatus::get_CallerId, get_CallerId
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
 - IFaxStatus::get_CallerId
 - faxcom/IFaxStatus::get_CallerId
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
 - IFaxStatus.CallerId
 - IFaxStatus.get_CallerId
---

# IFaxStatus::get_CallerId


## -description

Retrieves the <b>CallerId</b> property for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>CallerId</b> property is a string that identifies the calling device that sent an inbound fax job.

This property is read-only.

## -parameters

## -remarks

If caller identification information is not available, the <b>IFaxStatus::get_CallerId</b> method returns an empty string.

The <b>IFaxStatus::get_CallerId</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>