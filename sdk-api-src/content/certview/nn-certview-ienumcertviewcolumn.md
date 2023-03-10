---
UID: NN:certview.IEnumCERTVIEWCOLUMN
title: IEnumCERTVIEWCOLUMN (certview.h)
description: Represents a column-enumeration sequence that contains the column data for the current row of the enumeration sequence.
helpviewer_keywords: ["IEnumCERTVIEWCOLUMN","IEnumCERTVIEWCOLUMN interface [Security]","IEnumCERTVIEWCOLUMN interface [Security]","described","_certsrv_ienumcertviewcolumn","certview/IEnumCERTVIEWCOLUMN","security.ienumcertviewcolumn"]
old-location: security\ienumcertviewcolumn.htm
tech.root: security
ms.assetid: 6e6547f9-44b2-4050-be90-ac8ede892adc
ms.date: 12/05/2018
ms.keywords: IEnumCERTVIEWCOLUMN, IEnumCERTVIEWCOLUMN interface [Security], IEnumCERTVIEWCOLUMN interface [Security],described, _certsrv_ienumcertviewcolumn, certview/IEnumCERTVIEWCOLUMN, security.ienumcertviewcolumn
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
 - IEnumCERTVIEWCOLUMN
 - certview/IEnumCERTVIEWCOLUMN
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
 - IEnumCERTVIEWCOLUMN
---

# IEnumCERTVIEWCOLUMN interface


## -description

The <b>IEnumCERTVIEWCOLUMN</b> interface represents a column-enumeration sequence that contains the column data for the current row of the enumeration sequence.

The column-enumeration sequence is obtained by a call to the <a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-enumcertviewcolumn">IEnumCERTVIEWROW::EnumCertViewColumn</a> method. After this enumeration sequence is obtained, the methods of the <b>IEnumCERTVIEWCOLUMN</b> interface can be used to perform the following tasks:<ul>
<li>Navigate through the enumeration.</li>
<li>Retrieve  data from each column.</li>
<li>Clone an exact copy of the enumeration sequence.</li>
</ul>


<b>IEnumCERTVIEWCOLUMN</b> is defined in Certview.h. When you create your program, however, use Certsrv.h as the include file. Certadm.dll provides the <b>IEnumCERTVIEWCOLUMN</b> interface. The type information for this interface is also in Certadml.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>IEnumCERTVIEWCOLUMN</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IEnumCERTVIEWCOLUMN</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/certview/nf-certview-icertview-enumcertviewcolumn">ICertView::EnumCertViewColumn</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-enumcertviewcolumn">IEnumCERTVIEWROW::EnumCertViewColumn</a>
