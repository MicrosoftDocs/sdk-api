---
UID: NF:faxcom.IFaxStatus.get_RecipientName
title: IFaxStatus::get_RecipientName (faxcom.h)
description: Retrieves the RecipientName property for a FaxStatus object. The RecipientName property is a null-terminated string that contains the name of the recipient of an inbound fax transmission.
helpviewer_keywords: ["IFaxStatus interface [Fax Service]","RecipientName property","IFaxStatus.RecipientName","IFaxStatus.get_RecipientName","IFaxStatus::RecipientName","IFaxStatus::get_RecipientName","RecipientName property [Fax Service]","RecipientName property [Fax Service]","IFaxStatus interface","_mfax_ifaxstatus_get_recipientname","fax._mfax_ifaxstatus_get_recipientname","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_recipientname_cpp","faxcom/IFaxStatus::RecipientName","faxcom/IFaxStatus::get_RecipientName","get_RecipientName"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_recipientname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6qlh.htm
ms.date: 12/05/2018
ms.keywords: IFaxStatus interface [Fax Service],RecipientName property, IFaxStatus.RecipientName, IFaxStatus.get_RecipientName, IFaxStatus::RecipientName, IFaxStatus::get_RecipientName, RecipientName property [Fax Service], RecipientName property [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_get_recipientname, fax._mfax_ifaxstatus_get_recipientname, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_recipientname_cpp, faxcom/IFaxStatus::RecipientName, faxcom/IFaxStatus::get_RecipientName, get_RecipientName
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
 - IFaxStatus::get_RecipientName
 - faxcom/IFaxStatus::get_RecipientName
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
 - IFaxStatus.RecipientName
 - IFaxStatus.get_RecipientName
---

# IFaxStatus::get_RecipientName


## -description

Retrieves the <b>RecipientName</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object. The <b>RecipientName</b> property is a null-terminated string that contains the name of the recipient of an inbound fax transmission.

This property is read-only.

## -parameters

## -remarks

If the information is not available, the <b>IFaxStatus::get_RecipientName</b> method returns an empty string. 

The <b>IFaxStatus::get_RecipientName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-receive-vb">IFaxStatus::get_Receive</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>