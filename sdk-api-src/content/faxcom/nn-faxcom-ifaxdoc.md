---
UID: NN:faxcom.IFaxDoc
title: IFaxDoc (faxcom.h)
description: The IFaxDoc dual interface is used by a fax client application to transmit fax documents and cover pages.
helpviewer_keywords: ["IFaxDoc","IFaxDoc interface [Fax Service]","IFaxDoc interface [Fax Service]","described","_mfax_ifaxdoc","fax._mfax_ifaxdoc","faxcom/IFaxDoc"]
old-location: fax\_mfax_ifaxdoc.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6mub.htm
ms.date: 12/05/2018
ms.keywords: IFaxDoc, IFaxDoc interface [Fax Service], IFaxDoc interface [Fax Service],described, _mfax_ifaxdoc, fax._mfax_ifaxdoc, faxcom/IFaxDoc
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
 - IFaxDoc
 - faxcom/IFaxDoc
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
 - IFaxDoc
---

# IFaxDoc interface


## -description

The <b>IFaxDoc</b> dual interface is used by a fax client application to transmit fax documents and cover pages. The interface retrieves and sets information about <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> objects. Information includes the name of the file to transmit, the fax number to which the fax server should send the fax, cover page settings, and other optional fax recipient and sender information.

## -inheritance

The <b>IFaxDoc</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxDoc</b> also has these types of members:

## -remarks

The <b>IFaxDoc</b> interface includes the following methods:

<ul>
<li>A method to send a fax document.</li>
<li>Property methods to set and retrieve individual property values associated with a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object.</li>
</ul>
<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxDoc</b> interface to send a fax document. You can also use the <b>IFaxDoc</b> interface to retrieve and set the properties of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object.

A client application should not call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve an <b>IFaxDoc</b> interface pointer. Instead, the application must perform the following steps to create an instance of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object: 
                

<ol>
<li>Call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve a pointer to an <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a> interface.</li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-connect-client-vb">IFaxServer::Connect</a> method to connect to an active fax server. </li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-createdocument-vb">IFaxServer::CreateDocument</a> method to create and initialize a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object for the connected fax server. (After calling the <b>IFaxServer::CreateDocument</b> method, you can also call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxDoc</b> interface pointer.)</li>
<li>Use the <b>IDispatch</b> interface pointer to call <b>IFaxDoc</b> interface methods.</li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-disconnect-client-vb">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method to destroy the <b>IFaxDoc</b> interface pointer, and the parent <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a> interface pointer.</li>
</ol>
The property methods of the <b>IFaxDoc</b> interface get or set the properties described following. If the property supports read access, the <b>IFaxDoc</b> interface includes a <i>get_PropertyName</i> method. If the property supports write access, the interface includes a <i>put_PropertyName</i> method.

Values are not required for optional properties that appear only on the cover page. The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-filename-vb">FileName</a> property is required to send a fax transmission using a call to the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-send-vb">IFaxDoc::Send</a> method. The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-faxnumber-vb">FaxNumber</a> property is also required.

The fax server can supply data from the registry for many properties that begin with <b>Sender</b>. The fax server supplies values if they have been entered under the <b>User Information</b> tab accessed through the Fax icon in Control Panel.

Following are the properties associated with a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
