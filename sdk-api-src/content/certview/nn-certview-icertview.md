---
UID: NN:certview.ICertView
title: ICertView (certview.h)
description: Allows properly authorized clients to create a customized or complete view of the Certificate Services database.
helpviewer_keywords: ["ICertView","ICertView interface [Security]","ICertView interface [Security]","described","_certsrv_icertview","certview/ICertView","security.icertview"]
old-location: security\icertview.htm
tech.root: security
ms.assetid: 0b6660ee-458f-457f-8a38-0d950aee2710
ms.date: 12/05/2018
ms.keywords: ICertView, ICertView interface [Security], ICertView interface [Security],described, _certsrv_icertview, certview/ICertView, security.icertview
req.header: certview.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertView
 - certview/ICertView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertView
---

# ICertView interface


## -description

The <b>ICertView</b> interface allows properly authorized clients to create a customized or complete view of the Certificate Services database.

The <b>ICertView</b> interface is used to perform the following tasks:<ul>
<li>Establish a connection with a Certificate Services server.</li>
<li>Obtain a row-enumeration sequence of the rows in the Certificate Services database.</li>
<li>Obtain a column-enumeration sequence for the columns of a row in the Certificate Services database.</li>
<li>Get the column count and index.</li>
<li>Specify sorting and qualifying restrictions for a column.</li>
<li>Specify the number of columns and a specific column in a customized view.</li>
</ul>


In C++, the <b>ICertView</b> interface is instantiated through a call to the COM function <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>. If, on the other hand, you are using Visual Basic Scripting Edition, you will need to reference the CertAdm Type library in your project and then instantiate the <a href="/windows/desktop/api/certview/nn-certview-icertview2">CCertView</a> object  by a call to 'New'. The sample code for the  
<a href="/windows/desktop/api/certview/nf-certview-icertview-openconnection">ICertView::OpenConnection</a> method illustrates the instantiation techniques.

The <b>ICertView</b> interface is defined in Certview.h. When you create your program, however, use Certsrv.h as the include file. Certadm.dll provides the <b>ICertView</b> interface. The type information for this interface is also in Certadml.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>ICertView</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertView</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewcolumn">IEnumCERTVIEWCOLUMN</a>



<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewrow">IEnumCERTVIEWROW</a>
