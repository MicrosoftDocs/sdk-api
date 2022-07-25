---
UID: NE:objidl.tagGLOBALOPT_UNMARSHALING_POLICY_VALUES
title: GLOBALOPT_UNMARSHALING_POLICY_VALUES (objidl.h)
description: Provides values for the COM unmarshaling policy global option.
helpviewer_keywords: ["COMGLB_UNMARSHALING_POLICY_HYBRID","COMGLB_UNMARSHALING_POLICY_NORMAL","COMGLB_UNMARSHALING_POLICY_STRONG","GLOBALOPT_UNMARSHALING_POLICY_VALUES","GLOBALOPT_UNMARSHALING_POLICY_VALUES enumeration [COM]","com.globalopt_unmarshaling_policy_values","objidl/COMGLB_UNMARSHALING_POLICY_HYBRID","objidl/COMGLB_UNMARSHALING_POLICY_NORMAL","objidl/COMGLB_UNMARSHALING_POLICY_STRONG","objidl/GLOBALOPT_UNMARSHALING_POLICY_VALUES"]
old-location: com\globalopt_unmarshaling_policy_values.htm
tech.root: com
ms.assetid: 7F557290-7162-4B32-880B-9A445A083F91
ms.date: 12/05/2018
ms.keywords: COMGLB_UNMARSHALING_POLICY_HYBRID, COMGLB_UNMARSHALING_POLICY_NORMAL, COMGLB_UNMARSHALING_POLICY_STRONG, GLOBALOPT_UNMARSHALING_POLICY_VALUES, GLOBALOPT_UNMARSHALING_POLICY_VALUES enumeration [COM], com.globalopt_unmarshaling_policy_values, objidl/COMGLB_UNMARSHALING_POLICY_HYBRID, objidl/COMGLB_UNMARSHALING_POLICY_NORMAL, objidl/COMGLB_UNMARSHALING_POLICY_STRONG, objidl/GLOBALOPT_UNMARSHALING_POLICY_VALUES
req.header: objidl.h
req.include-header: Objidlbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidlbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: GLOBALOPT_UNMARSHALING_POLICY_VALUES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagGLOBALOPT_UNMARSHALING_POLICY_VALUES
 - objidl/tagGLOBALOPT_UNMARSHALING_POLICY_VALUES
 - GLOBALOPT_UNMARSHALING_POLICY_VALUES
 - objidl/GLOBALOPT_UNMARSHALING_POLICY_VALUES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidl.h
api_name:
 - GLOBALOPT_UNMARSHALING_POLICY_VALUES
---

# GLOBALOPT_UNMARSHALING_POLICY_VALUES enumeration


## -description

Provides values for the COM unmarshaling policy global option.

## -enum-fields

### -field COMGLB_UNMARSHALING_POLICY_NORMAL:0

Unmarshaling behavior is the same as versions older than Windows 8. <b>EOAC_NO_CUSTOM_MARSHAL</b> restrictions apply if this flag is set in <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>. Otherwise, there are no restrictions. This is the default for processes that aren't in the app container.

### -field COMGLB_UNMARSHALING_POLICY_STRONG:1

Unmarshaling allows only a system-trusted list of hardened unmarshalers and unmarshalers allowed per-process by the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coallowunmarshalerclsid">CoAllowUnmarshalerCLSID</a> function. This is the default for processes in the app container.

### -field COMGLB_UNMARSHALING_POLICY_HYBRID:2

Unmarshaling data whose source is app container allows only a system-trusted list of hardened unmarshalers and unmarshalers allowed per-process by the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coallowunmarshalerclsid">CoAllowUnmarshalerCLSID</a> function. Unmarshaling behavior for data with a source that's not app container is unchanged from previous versions.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iglobaloptions">IGlobalOptions</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imarshalingstream">IMarshalingStream</a>
