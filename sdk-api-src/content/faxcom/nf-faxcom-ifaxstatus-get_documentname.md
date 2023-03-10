---
UID: NF:faxcom.IFaxStatus.get_DocumentName
title: IFaxStatus::get_DocumentName (faxcom.h)
description: Retrieves the DocumentName property for the FaxStatus object of a parent FaxPort object. The DocumentName property is a null-terminated string that contains the user-friendly name associated with an active fax document.
helpviewer_keywords: ["DocumentName property [Fax Service]","DocumentName property [Fax Service]","IFaxStatus interface","IFaxStatus interface [Fax Service]","DocumentName property","IFaxStatus.DocumentName","IFaxStatus.get_DocumentName","IFaxStatus::DocumentName","IFaxStatus::get_DocumentName","_mfax_ifaxstatus_get_documentname","fax._mfax_ifaxstatus_get_documentname","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_documentname_cpp","faxcom/IFaxStatus::DocumentName","faxcom/IFaxStatus::get_DocumentName","get_DocumentName"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_documentname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6jvp.htm
ms.date: 12/05/2018
ms.keywords: DocumentName property [Fax Service], DocumentName property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],DocumentName property, IFaxStatus.DocumentName, IFaxStatus.get_DocumentName, IFaxStatus::DocumentName, IFaxStatus::get_DocumentName, _mfax_ifaxstatus_get_documentname, fax._mfax_ifaxstatus_get_documentname, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_documentname_cpp, faxcom/IFaxStatus::DocumentName, faxcom/IFaxStatus::get_DocumentName, get_DocumentName
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
 - IFaxStatus::get_DocumentName
 - faxcom/IFaxStatus::get_DocumentName
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
 - IFaxStatus.DocumentName
 - IFaxStatus.get_DocumentName
---

# IFaxStatus::get_DocumentName


## -description

Retrieves the <b>DocumentName</b> property for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>DocumentName</b> property is a null-terminated string that contains the user-friendly name associated with an active fax document.

This property is read-only.

## -parameters

## -remarks

You can use the <b>DocumentName</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object in conjunction with the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-documentsize-vb">DocumentSize</a> property of the object to inform users about the size of outbound jobs. 

The <b>IFaxStatus::get_DocumentName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-documentsize-vb">IFaxStatus::get_DocumentSize</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>