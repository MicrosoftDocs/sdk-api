---
UID: NS:naptypes.tagFailureCategoryMapping
title: FailureCategoryMapping (naptypes.h)
description: Contains optional compliance state information that is returned by the System Health Validator (SHV).
helpviewer_keywords: ["FailureCategoryMapping","FailureCategoryMapping structure [NAP]","nap.failurecategorymapping_struct","naptypes/FailureCategoryMapping"]
old-location: nap\failurecategorymapping_struct.htm
tech.root: NAP
ms.assetid: dbf2978f-062a-417b-a6df-a82879e10ec8
ms.date: 12/05/2018
ms.keywords: FailureCategoryMapping, FailureCategoryMapping structure [NAP], nap.failurecategorymapping_struct, naptypes/FailureCategoryMapping
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FailureCategoryMapping
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagFailureCategoryMapping
 - naptypes/tagFailureCategoryMapping
 - FailureCategoryMapping
 - naptypes/FailureCategoryMapping
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - FailureCategoryMapping
---

# FailureCategoryMapping structure


## -description

<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>FailureCategoryMapping</b> structure contains optional compliance state information that is returned by the System Health Validator (SHV).

## -struct-fields

### -field mappingCompliance

An array of        <b>BOOLs</b> that contain the compliance state of each <a href="/windows/desktop/api/naptypes/ne-naptypes-failurecategory">FailureCategory</a>.  <b>TRUE</b> indicates the category is compliant and <b>FALSE</b> indicates non-compliance. 

<div class="alert"><b>Note</b>  The length of <b>mappingCompliance</b> is defined by <a href="/windows/desktop/NAP/nap-type-constants">failureCategoryCount</a>.</div>
<div> </div>

## -remarks

If a failure occurs in the system (for example, a component or communication failures), the SHV may return
   an <a href="/windows/desktop/NAP/sohattributetype-enum">sohAttributeTypeFailureCategory</a> type type-length-value (TLV) object in its <a href="/windows/desktop/api/naptypes/ns-naptypes-soh">SoHResponse</a> instead
   of making a compliance decision. In turn, the NAP system maps the <a href="/windows/desktop/api/naptypes/ne-naptypes-failurecategory">FailureCategory</a> type returned by the TLV object to compliant or non-compliant within the <b>FailureCategoryMapping</b> structure as follows:

<ul>
<li>mappingCompliance[0] = mapping for <a href="/windows/desktop/api/naptypes/ne-naptypes-failurecategory">failureCategoryOther</a>
</li>
<li>mappingCompliance[1] = mapping for <a href="/windows/desktop/api/naptypes/ne-naptypes-failurecategory">failureCategoryClientComponent</a>
</li>
<li>mappingCompliance[2] = mapping for <a href="/windows/desktop/api/naptypes/ne-naptypes-failurecategory">failureCategoryClientCommunication</a>
</li>
<li>mappingCompliance[3] = mapping for <a href="/windows/desktop/api/naptypes/ne-naptypes-failurecategory">failureCategoryServerComponent</a>
</li>
<li>mappingCompliance[4] = mapping for <a href="/windows/desktop/api/naptypes/ne-naptypes-failurecategory">failureCategoryServerCommunication</a>
</li>
</ul>
By default, all categories map to non-compliant (FALSE).

## -see-also

<a href="/windows/desktop/api/naptypes/ne-naptypes-failurecategory">FailureCategory</a>