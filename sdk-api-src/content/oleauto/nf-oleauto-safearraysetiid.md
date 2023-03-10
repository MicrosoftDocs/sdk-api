---
UID: NF:oleauto.SafeArraySetIID
title: SafeArraySetIID function (oleauto.h)
description: Sets the GUID of the interface for the specified safe array.
helpviewer_keywords: ["SafeArraySetIID","SafeArraySetIID function [Automation]","_oa96_SafeArraySetIID","automat.safearraysetiid","oleauto/SafeArraySetIID"]
old-location: automat\safearraysetiid.htm
tech.root: automat
ms.assetid: 851b8a44-9da4-418c-88bc-80c9fc55d25c
ms.date: 12/05/2018
ms.keywords: SafeArraySetIID, SafeArraySetIID function [Automation], _oa96_SafeArraySetIID, automat.safearraysetiid, oleauto/SafeArraySetIID
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
 - SafeArraySetIID
 - oleauto/SafeArraySetIID
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
 - SafeArraySetIID
---

# SafeArraySetIID function


## -description

Sets the GUID of the interface for the specified safe array.

## -parameters

### -param psa [in]

The safe array descriptor.

### -param guid [in]

The IID.

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
The argument <i>psa</i> is null or the array descriptor does not have the FADF_HAVEIID flag set.

</td>
</tr>
</table>

