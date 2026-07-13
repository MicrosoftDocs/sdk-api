---
UID: NF:oleauto.DispGetIDsOfNames
title: DispGetIDsOfNames function (oleauto.h)
description: Low-level helper for Invoke that provides machine independence for customized Invoke. (DispGetIDsOfNames)
helpviewer_keywords: ["DispGetIDsOfNames","DispGetIDsOfNames function [Automation]","_oa96_DispGetIDsOfNames","automat.dispgetidsofnames","oleauto/DispGetIDsOfNames"]
old-location: automat\dispgetidsofnames.htm
tech.root: automat
ms.assetid: 720a0237-9c68-4252-9f66-43610d4be106
ms.date: 12/05/2018
ms.keywords: DispGetIDsOfNames, DispGetIDsOfNames function [Automation], _oa96_DispGetIDsOfNames, automat.dispgetidsofnames, oleauto/DispGetIDsOfNames
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
 - DispGetIDsOfNames
 - oleauto/DispGetIDsOfNames
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
 - DispGetIDsOfNames
---

# DispGetIDsOfNames function


## -description

Low-level helper for <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">Invoke</a> that provides machine independence for customized <b>Invoke</b>.

## -parameters

### -param ptinfo

The type information for an interface. This type information is specific to one interface and language code, so it is not necessary to pass an interface identifier (IID) or LCID to this function.

### -param rgszNames [in]

An array of name strings that can be the same array passed to DispInvoke in the DISPPARAMS structure. If <i>cNames</i> is greater than 1, the first name is interpreted as a method name, and subsequent names are interpreted as parameters to that method.

### -param cNames

The number of elements in <i>rgszNames</i>.

### -param rgdispid [out]

An array of DISPIDs to be filled in by this function. The first ID corresponds to the method name. Subsequent IDs are interpreted as parameters to the method.

## -returns

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
The interface is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_UNKNOWNNAME
</b></dt>
</dl>
</td>
<td width="60%">
One or more of the specified names were not known. The returned array of DISPIDs contains DISPID_UNKNOWN for each entry that corresponds to an unknown name.


</td>
</tr>
</table>
 

Any of the <b>ITypeInfo::Invoke</b> errors can also be returned.
