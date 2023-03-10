---
UID: NF:oleauto.SafeArrayUnaccessData
title: SafeArrayUnaccessData function (oleauto.h)
description: Decrements the lock count of an array, and invalidates the pointer retrieved by SafeArrayAccessData.
helpviewer_keywords: ["SafeArrayUnaccessData","SafeArrayUnaccessData function [Automation]","_oa96_SafeArrayUnaccessData","automat.safearrayunaccessdata","oleauto/SafeArrayUnaccessData"]
old-location: automat\safearrayunaccessdata.htm
tech.root: automat
ms.assetid: 61b482cb-f0a3-4efb-9a68-f373f241e89a
ms.date: 12/05/2018
ms.keywords: SafeArrayUnaccessData, SafeArrayUnaccessData function [Automation], _oa96_SafeArrayUnaccessData, automat.safearrayunaccessdata, oleauto/SafeArrayUnaccessData
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
 - SafeArrayUnaccessData
 - oleauto/SafeArrayUnaccessData
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
 - SafeArrayUnaccessData
---

# SafeArrayUnaccessData function


## -description

Decrements the lock count of an array, and invalidates the pointer retrieved by <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayaccessdata">SafeArrayAccessData</a>.

## -parameters

### -param psa [in]

An array descriptor created by <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreate">SafeArrayCreate</a>.

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
The argument <i>psa</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The array could not be unlocked.

</td>
</tr>
</table>