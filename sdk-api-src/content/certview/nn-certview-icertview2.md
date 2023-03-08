---
UID: NN:certview.ICertView2
title: ICertView2 (certview.h)
description: Allow properly authorized clients to create a customized or complete view of the Certificate Services database.
helpviewer_keywords: ["ICertView2","ICertView2 interface [Security]","ICertView2 interface [Security]","described","_certsrv_icertview2","certview/ICertView2","security.icertview2"]
old-location: security\icertview2.htm
tech.root: security
ms.assetid: c29f1db3-0cdf-463e-a202-47fbba8e1c81
ms.date: 12/05/2018
ms.keywords: ICertView2, ICertView2 interface [Security], ICertView2 interface [Security],described, _certsrv_icertview2, certview/ICertView2, security.icertview2
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
 - ICertView2
 - certview/ICertView2
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
 - ICertView2
---

# ICertView2 interface


## -description

The <b>ICertView2</b> interface is one of two interfaces that allow properly authorized clients to create a customized or complete view of the Certificate Services database.

The <b>ICertView2</b> interface is used to perform the following tasks:<ul>
<li>Establish a connection with a Certificate Services server.</li>
<li>Obtain a row-enumeration sequence of the rows in the Certificate Services database.</li>
<li>Obtain a column-enumeration sequence for the schema in the Certificate Services database.</li>
<li>Get the column count and index.</li>
<li>Specify sorting and qualifying restrictions for a column.</li>
<li>Specify the number of columns and a specific column in a customized view.</li>
<li>Specify which tables are used by subsequent calls to <b>ICertView2</b> methods (introduced by <b>ICertView2</b>).</li>
</ul>


In C++, the <b>ICertView2</b> interface is instantiated through a call to the COM function <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>. If, on the other hand, you are using Visual Basic Scripting Edition, you will need to reference the CertAdm Type library in your project and then instantiate the <b>CCertView</b> object by a call to 'New'.  The sample code for the  
<a href="/windows/desktop/api/certview/nf-certview-icertview-openconnection">OpenConnection</a> method illustrates the instantiation techniques.

The <b>ICertView2</b> interface is defined in Certview.h. When you create your program, however, use Certsrv.h as the include file. Certadm.dll provides the <b>ICertView2</b> interface. The type information for this interface is also in Certadml.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>ICertView2</b> interface inherits from <a href="/windows/desktop/api/certview/nn-certview-icertview">ICertView</a> and <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>. <b>ICertView2</b> also has these types of members:

