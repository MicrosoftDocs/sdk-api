---
UID: NF:faxcom.IFaxStatus.get_SenderName
title: IFaxStatus::get_SenderName (faxcom.h)
description: Retrieves the SenderName property for the FaxStatus object of a parent FaxPort object. The SenderName property is a null-terminated string that contains the name of the user who sent the fax transmission.
helpviewer_keywords: ["IFaxStatus interface [Fax Service]","SenderName property","IFaxStatus.SenderName","IFaxStatus.get_SenderName","IFaxStatus::SenderName","IFaxStatus::get_SenderName","SenderName property [Fax Service]","SenderName property [Fax Service]","IFaxStatus interface","_mfax_ifaxstatus_get_sendername","fax._mfax_ifaxstatus_get_sendername","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_sendername_cpp","faxcom/IFaxStatus::SenderName","faxcom/IFaxStatus::get_SenderName","get_SenderName"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_sendername_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_54x1.htm
ms.date: 12/05/2018
ms.keywords: IFaxStatus interface [Fax Service],SenderName property, IFaxStatus.SenderName, IFaxStatus.get_SenderName, IFaxStatus::SenderName, IFaxStatus::get_SenderName, SenderName property [Fax Service], SenderName property [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_get_sendername, fax._mfax_ifaxstatus_get_sendername, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_sendername_cpp, faxcom/IFaxStatus::SenderName, faxcom/IFaxStatus::get_SenderName, get_SenderName
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
 - IFaxStatus::get_SenderName
 - faxcom/IFaxStatus::get_SenderName
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
 - IFaxStatus.SenderName
 - IFaxStatus.get_SenderName
---

# IFaxStatus::get_SenderName


## -description

Retrieves the <b>SenderName</b> property for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>SenderName</b> property is a null-terminated string that contains the name of the user who sent the fax transmission.

This property is read-only.

## -parameters

## -remarks

If the sender's name is not available, the <b>IFaxStatus::get_SenderName</b> method returns an empty string.

The <b>IFaxStatus::get_SenderName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-send-vb">IFaxStatus::get_Send</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>