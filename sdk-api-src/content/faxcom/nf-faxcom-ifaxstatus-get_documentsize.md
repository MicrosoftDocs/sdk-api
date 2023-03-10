---
UID: NF:faxcom.IFaxStatus.get_DocumentSize
title: IFaxStatus::get_DocumentSize (faxcom.h)
description: Retrieves the DocumentSize property for the FaxStatus object of a parent FaxPort object. The DocumentSize property is the size of the fax document associated with the active outbound job on a specific port.
helpviewer_keywords: ["DocumentSize property [Fax Service]","DocumentSize property [Fax Service]","IFaxStatus interface","IFaxStatus interface [Fax Service]","DocumentSize property","IFaxStatus.DocumentSize","IFaxStatus.get_DocumentSize","IFaxStatus::DocumentSize","IFaxStatus::get_DocumentSize","_mfax_ifaxstatus_get_documentsize","fax._mfax_ifaxstatus_get_documentsize","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_documentsize_cpp","faxcom/IFaxStatus::DocumentSize","faxcom/IFaxStatus::get_DocumentSize","get_DocumentSize"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_documentsize_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5d5x.htm
ms.date: 12/05/2018
ms.keywords: DocumentSize property [Fax Service], DocumentSize property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],DocumentSize property, IFaxStatus.DocumentSize, IFaxStatus.get_DocumentSize, IFaxStatus::DocumentSize, IFaxStatus::get_DocumentSize, _mfax_ifaxstatus_get_documentsize, fax._mfax_ifaxstatus_get_documentsize, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_documentsize_cpp, faxcom/IFaxStatus::DocumentSize, faxcom/IFaxStatus::get_DocumentSize, get_DocumentSize
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
 - IFaxStatus::get_DocumentSize
 - faxcom/IFaxStatus::get_DocumentSize
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
 - IFaxStatus.DocumentSize
 - IFaxStatus.get_DocumentSize
---

# IFaxStatus::get_DocumentSize


## -description

Retrieves the <b>DocumentSize</b> property for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>DocumentSize</b> property is the size of the fax document associated with the active outbound job on a specific port.

This property is read-only.

## -parameters

## -remarks

You can use the <b>DocumentSize</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object in conjunction with the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-documentname-vb">DocumentName</a> property of the object to inform users about the size of outbound jobs.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-documentname-vb">IFaxStatus::get_DocumentName</a>