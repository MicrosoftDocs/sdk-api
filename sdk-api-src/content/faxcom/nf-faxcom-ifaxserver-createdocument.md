---
UID: NF:faxcom.IFaxServer.CreateDocument
title: IFaxServer::CreateDocument (faxcom.h)
description: The IFaxServer::CreateDocument method creates a FaxDoc object for a specified FaxServer object. The FaxDoc object allows a user to create and transmit a document to one or more fax recipients.
helpviewer_keywords: ["CreateDocument","CreateDocument method [Fax Service]","CreateDocument method [Fax Service]","IFaxServer interface","IFaxServer interface [Fax Service]","CreateDocument method","IFaxServer.CreateDocument","IFaxServer::CreateDocument","_mfax_ifaxserver_createdocument","fax._mfax_ifaxserver_client_mfax_ifaxserver_createdocument_cpp","fax._mfax_ifaxserver_createdocument","faxcom/IFaxServer::CreateDocument"]
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_createdocument_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0cfo.htm
ms.date: 12/05/2018
ms.keywords: CreateDocument, CreateDocument method [Fax Service], CreateDocument method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],CreateDocument method, IFaxServer.CreateDocument, IFaxServer::CreateDocument, _mfax_ifaxserver_createdocument, fax._mfax_ifaxserver_client_mfax_ifaxserver_createdocument_cpp, fax._mfax_ifaxserver_createdocument, faxcom/IFaxServer::CreateDocument
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
 - IFaxServer::CreateDocument
 - faxcom/IFaxServer::CreateDocument
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
 - IFaxServer.CreateDocument
 - IFaxServer.CreateDocument
---

# IFaxServer::CreateDocument


## -description

The <b>IFaxServer::CreateDocument</b> method creates a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object for a specified <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The FaxDoc object allows a user to create and transmit a document to one or more fax recipients.

## -parameters

### -param FileName [in]

Type: <b>BSTR</b>

Specifies a null-terminated string that contains the fully qualified path and name of the file that contains the fax document to transmit. The path can be a UNC path or a path beginning with a drive letter.

This parameter can contain any valid local or remote file name. The file must be a properly registered file type, and the fax server must be able to access the file.

### -param retval [out]

Type: <b>VARIANT*</b>

Pointer to a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure that receives an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The method returns a pdispVal member with a VT_DISPATCH data type.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>IFaxServer::CreateDocument</b> method retrieves an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. A fax client application can also access the <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a> interface directly by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to retrieve an interface pointer. The <b>IFaxDoc</b> interface allows a user to set the properties for a fax document, and then transmit the document.

A fax client application should not call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve an <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a> interface pointer because it will not be instantiated correctly.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a>



<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>