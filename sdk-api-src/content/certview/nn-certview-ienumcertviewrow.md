---
UID: NN:certview.IEnumCERTVIEWROW
title: IEnumCERTVIEWROW (certview.h)
description: Represents a row-enumeration sequence that contains the data in the rows of the Certificate Services view, allowing further access to the columns, attributes, and extensions associated with each row.
helpviewer_keywords: ["IEnumCERTVIEWROW","IEnumCERTVIEWROW interface [Security]","IEnumCERTVIEWROW interface [Security]","described","_certsrv_ienumcertviewrow","certview/IEnumCERTVIEWROW","security.ienumcertviewrow"]
old-location: security\ienumcertviewrow.htm
tech.root: security
ms.assetid: c9529f7a-9d97-4315-af96-f7b687af3c2e
ms.date: 12/05/2018
ms.keywords: IEnumCERTVIEWROW, IEnumCERTVIEWROW interface [Security], IEnumCERTVIEWROW interface [Security],described, _certsrv_ienumcertviewrow, certview/IEnumCERTVIEWROW, security.ienumcertviewrow
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
 - IEnumCERTVIEWROW
 - certview/IEnumCERTVIEWROW
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
 - IEnumCERTVIEWROW
 - IEnumCERTVIEWROW.Clone
---

# IEnumCERTVIEWROW interface


## -description

The <b>IEnumCERTVIEWROW</b> interface represents a row-enumeration sequence that contains the data in the rows of the Certificate Services view, allowing further access to the columns, attributes, and extensions associated with each row.

The row-enumeration sequence is obtained through a call to the 
<a href="/windows/desktop/api/certview/nf-certview-icertview-openview">ICertView::OpenView</a> method. After this enumeration sequence is obtained, the <b>IEnumCERTVIEWROW</b> methods can be used to perform the following tasks:<ul>
<li>Navigate through the enumeration sequence.</li>
<li>Obtain other objects for enumerating the columns, certificate extensions, or attributes associated with a specific row.</li>
<li>Retrieve the maximum number of rows for the view.</li>
</ul>


<b>IEnumCERTVIEWROW</b> is defined in Certview.h. When you create your program, however, use Certsrv.h as the include file. Certadm.dll provides the <b>IEnumCERTVIEWROW</b> interface. The type information for this interface is also in Certadml.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>IEnumCERTVIEWROW</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IEnumCERTVIEWROW</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/certview/nf-certview-icertview-openview">ICertView</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
