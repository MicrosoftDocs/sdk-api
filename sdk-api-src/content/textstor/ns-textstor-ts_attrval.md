---
UID: NS:textstor.TS_ATTRVAL
title: TS_ATTRVAL (textstor.h)
description: The TS_ATTRVAL structure contains document attribute values.
helpviewer_keywords: ["TS_ATTRVAL","TS_ATTRVAL structure [Text Services Framework]","_tsf_ts_attrval_ref","textstor/TS_ATTRVAL","tsf.ts_attrval"]
old-location: tsf\ts_attrval.htm
tech.root: TSF
ms.assetid: 9209ef60-6a1d-4aad-9f9f-775534116f37
ms.date: 12/05/2018
ms.keywords: TS_ATTRVAL, TS_ATTRVAL structure [Text Services Framework], _tsf_ts_attrval_ref, textstor/TS_ATTRVAL, tsf.ts_attrval
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TS_ATTRVAL
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TS_ATTRVAL
 - textstor/TS_ATTRVAL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Textstor.h
api_name:
 - TS_ATTRVAL
---

# TS_ATTRVAL structure


## -description

The <b>TS_ATTRVAL</b> structure contains document attribute values.

## -struct-fields

### -field idAttr

GUID for the attribute type.

### -field dwOverlapId

A unique identifier of this attribute when overlapped with other attributes. This is a feature in <a href="/previous-versions/ms971350(v=msdn.10)">Microsoft Active Accessibility</a>. In TSF, this parameter value is zero (0). Any nonzero value is ignored.

### -field varValue

Value of the attribute.

## -remarks

An application uses attributes to expose its data to TSF, whereas text services use properties to expose their data to TSF. <b>TS_ATTRVAL</b> is used in <a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a> and <a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a> methods.

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition">ITextStoreACP::RequestAttrsTransitioningAtPosition
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-requestsupportedattrs">ITextStoreACP::RequestSupportedAttrs
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-retrieverequestedattrs">ITextStoreACP::RetrieveRequestedAttrs
      </a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition">ITextStoreAnchor::RequestAttrsTransitioningAtPosition
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-requestsupportedattrs">ITextStoreAnchor::RequestSupportedAttrs
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-retrieverequestedattrs">ITextStoreAnchor::RetrieveRequestedAttrs
      </a>



<a href="/previous-versions/ms971350(v=msdn.10)">Microsoft Active Accessibility</a>



<a href="/windows/desktop/api/msctf/ns-msctf-tf_propertyval">TF_PROPERTYVAL
      </a>



<a href="/windows/desktop/TSF/ts-attrid">TS_ATTRID
      </a>