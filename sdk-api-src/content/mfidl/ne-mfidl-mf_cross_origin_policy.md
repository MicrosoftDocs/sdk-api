---
UID: NE:mfidl._MF_CROSS_ORIGIN_POLICY
title: MF_CROSS_ORIGIN_POLICY (mfidl.h)
description: Maps to the W3C cross origin settings (CORS) attribute used by the HTML5 media element.
helpviewer_keywords: ["MF_CROSS_ORIGIN_POLICY","MF_CROSS_ORIGIN_POLICY_ANONYMOUS","MF_CROSS_ORIGIN_POLICY_NONE","MF_CROSS_ORIGIN_POLICY_USE_CREDENTIALS","_MF_CROSS_ORIGIN_POLICY","_MF_CROSS_ORIGIN_POLICY enumeration [Media Foundation]","mf._mf_cross_origin_policy","mfidl/MF_CROSS_ORIGIN_POLICY_ANONYMOUS","mfidl/MF_CROSS_ORIGIN_POLICY_NONE","mfidl/MF_CROSS_ORIGIN_POLICY_USE_CREDENTIALS","mfidl/_MF_CROSS_ORIGIN_POLICY"]
old-location: mf\_mf_cross_origin_policy.htm
tech.root: mf
ms.assetid: 77A8F413-5AA8-49E4-9846-A3F87FB878E7
ms.date: 12/05/2018
ms.keywords: MF_CROSS_ORIGIN_POLICY, MF_CROSS_ORIGIN_POLICY_ANONYMOUS, MF_CROSS_ORIGIN_POLICY_NONE, MF_CROSS_ORIGIN_POLICY_USE_CREDENTIALS, _MF_CROSS_ORIGIN_POLICY, _MF_CROSS_ORIGIN_POLICY enumeration [Media Foundation], mf._mf_cross_origin_policy, mfidl/MF_CROSS_ORIGIN_POLICY_ANONYMOUS, mfidl/MF_CROSS_ORIGIN_POLICY_NONE, mfidl/MF_CROSS_ORIGIN_POLICY_USE_CREDENTIALS, mfidl/_MF_CROSS_ORIGIN_POLICY
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MF_CROSS_ORIGIN_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MF_CROSS_ORIGIN_POLICY
 - mfidl/_MF_CROSS_ORIGIN_POLICY
 - MF_CROSS_ORIGIN_POLICY
 - mfidl/MF_CROSS_ORIGIN_POLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - _MF_CROSS_ORIGIN_POLICY
---

# MF_CROSS_ORIGIN_POLICY enumeration


## -description



Maps to the W3C cross origin settings (CORS) attribute used by the HTML5 media element

## -enum-fields

### -field MF_CROSS_ORIGIN_POLICY_NONE:0

No CORS state.

### -field MF_CROSS_ORIGIN_POLICY_ANONYMOUS:1

 Requests for the element will have their mode set to "cors" and their credentials mode set to "same-origin".

### -field MF_CROSS_ORIGIN_POLICY_USE_CREDENTIALS:2

Requests for the element will have their mode set to "cors" and their credentials mode set to "include".

