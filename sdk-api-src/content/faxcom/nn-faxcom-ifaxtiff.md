---
UID: NN:faxcom.IFaxTiff
title: IFaxTiff (faxcom.h)
description: The IFaxTiff dual interface is used by a fax client application to retrieve information about FaxTiff objects.
helpviewer_keywords: ["IFaxTiff","IFaxTiff interface [Fax Service]","IFaxTiff interface [Fax Service]","described","_mfax_ifaxtiff","fax._mfax_ifaxtiff","faxcom/IFaxTiff"]
old-location: fax\_mfax_ifaxtiff.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3zhi.htm
ms.date: 12/05/2018
ms.keywords: IFaxTiff, IFaxTiff interface [Fax Service], IFaxTiff interface [Fax Service],described, _mfax_ifaxtiff, fax._mfax_ifaxtiff, faxcom/IFaxTiff
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
 - IFaxTiff
 - faxcom/IFaxTiff
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
 - IFaxTiff
---

# IFaxTiff interface


## -description

The <b>IFaxTiff</b> dual interface is used by a fax client application to retrieve information about <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> objects. A FaxTiff object represents a Tagged Image File Format Class F (TIFF Class F) file that the fax service has transmitted or received. The fax service embeds custom Tagged Image File Format (TIFF) tags in the file to store information about the fax transmission.

It is not necessary to be familiar with the structure of a TIFF file to use the <b>IFaxTiff</b> interface and access the attributes of <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> objects. This interface provides a convenient alternative to manually parsing the TIFF data in a fax file. The <b>IFaxTiff</b> interface includes the following property methods:
<ul>
<li>Property methods to set and retrieve the name of the fax file described by the <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object.</li>
<li>Property methods to retrieve other attributes of the <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object, such as device and station identifiers, the fax number, and sender and recipient names.</li>
</ul><div class="alert"><b>Note</b>  A fax client application must  set the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-image-vb">Image</a> property before retrieving another property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object.</div><div> </div>

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxTiff</b> interface to retrieve the properties of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object.

Call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve a pointer to an <b>IFaxTiff</b> interface and create an instance of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object. It is not necessary to call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-connect-client-vb">IFaxServer::Connect</a> method to initiate a connection with an active fax server. A fax server connection is not required to access the <b>IFaxTiff</b> interface.

The property methods of the <b>IFaxTiff</b> interface get or set the properties described following. If the property supports read access, the <b>IFaxTiff</b> interface includes a <i>get_PropertyName</i> method. If the property supports write access, the interface includes a <i>put_PropertyName</i> method.

Following are the properties associated with a <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>