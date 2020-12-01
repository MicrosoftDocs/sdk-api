---
UID: NF:faxcom.IFaxStatus.get_RoutingString
title: IFaxStatus::get_RoutingString (faxcom.h)
description: Retrieves the RoutingString property for the FaxStatus object of a parent FaxPort object. The RoutingString property is a null-terminated string that contains routing information for inbound fax transmissions that is specific to a fax service provider.
helpviewer_keywords: ["IFaxStatus interface [Fax Service]","RoutingString property","IFaxStatus.RoutingString","IFaxStatus.get_RoutingString","IFaxStatus::RoutingString","IFaxStatus::get_RoutingString","RoutingString property [Fax Service]","RoutingString property [Fax Service]","IFaxStatus interface","_mfax_ifaxstatus_get_routingstring","fax._mfax_ifaxstatus_get_routingstring","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_routingstring_cpp","faxcom/IFaxStatus::RoutingString","faxcom/IFaxStatus::get_RoutingString","get_RoutingString"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_routingstring_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1aav.htm
ms.date: 12/05/2018
ms.keywords: IFaxStatus interface [Fax Service],RoutingString property, IFaxStatus.RoutingString, IFaxStatus.get_RoutingString, IFaxStatus::RoutingString, IFaxStatus::get_RoutingString, RoutingString property [Fax Service], RoutingString property [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_get_routingstring, fax._mfax_ifaxstatus_get_routingstring, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_routingstring_cpp, faxcom/IFaxStatus::RoutingString, faxcom/IFaxStatus::get_RoutingString, get_RoutingString
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
 - IFaxStatus::get_RoutingString
 - faxcom/IFaxStatus::get_RoutingString
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
 - IFaxStatus.RoutingString
 - IFaxStatus.get_RoutingString
---

# IFaxStatus::get_RoutingString


## -description

Retrieves the <b>RoutingString</b> property for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>RoutingString</b> property is a null-terminated string that contains routing information for inbound fax transmissions that is specific to a fax service provider.

This property is read-only.

## -parameters

## -remarks

The <b>IFaxStatus::get_RoutingString</b> method sets the <i>pVal</i> parameter to optional inbound routing information, if it is available. If the information is not available, the method returns an empty string.

The <b>IFaxStatus::get_RoutingString</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-receive-vb">IFaxStatus::get_Receive</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>