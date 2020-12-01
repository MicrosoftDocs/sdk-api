---
UID: NF:oleauto.SafeArrayGetVartype
title: SafeArrayGetVartype function (oleauto.h)
description: Gets the VARTYPE stored in the specified safe array.
helpviewer_keywords: ["SafeArrayGetVartype","SafeArrayGetVartype function [Automation]","_oa96_SafeArrayGetVartype","automat.safearraygetvartype","oleauto/SafeArrayGetVartype"]
old-location: automat\safearraygetvartype.htm
tech.root: automat
ms.assetid: 8ec0e736-bac8-4df4-ba32-433cd8478c55
ms.date: 12/05/2018
ms.keywords: SafeArrayGetVartype, SafeArrayGetVartype function [Automation], _oa96_SafeArrayGetVartype, automat.safearraygetvartype, oleauto/SafeArrayGetVartype
req.header: oleauto.h
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SafeArrayGetVartype
 - oleauto/SafeArrayGetVartype
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArrayGetVartype
---

# SafeArrayGetVartype function


## -description

Gets the VARTYPE stored in the specified safe array.

## -parameters

### -param psa [in]

An array descriptor created by <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreate">SafeArrayCreate</a>.

### -param pvt [out]

The VARTYPE.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is not valid.

</td>
</tr>
</table>

## -remarks

If FADF_HAVEVARTYPE is set, <b>SafeArrayGetVartype</b> returns the VARTYPE stored in the array descriptor. If FADF_RECORD is set, it returns VT_RECORD; if FADF_DISPATCH is set, it returns VT_DISPATCH; and if FADF_UNKNOWN is set, it returns VT_UNKNOWN.

<b>SafeArrayGetVartype</b> can fail to return VT_UNKNOWN for SAFEARRAY types that are based on <b>IUnknown</b>. Callers should additionally check whether the SAFEARRAY type's <b>fFeatures</b> field has the FADF_UNKNOWN flag set.

## -see-also

<a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY Data Type</a>