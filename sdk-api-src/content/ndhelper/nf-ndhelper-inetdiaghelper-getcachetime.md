---
UID: NF:ndhelper.INetDiagHelper.GetCacheTime
title: INetDiagHelper::GetCacheTime (ndhelper.h)
description: Specifies the time when cached results of a diagnosis and repair operation have expired.
helpviewer_keywords: ["GetCacheTime","GetCacheTime method [NDF]","GetCacheTime method [NDF]","INetDiagHelper interface","INetDiagHelper interface [NDF]","GetCacheTime method","INetDiagHelper.GetCacheTime","INetDiagHelper::GetCacheTime","ndf.inetdiaghelpe_getcachetime","ndhelper/INetDiagHelper::GetCacheTime"]
old-location: ndf\inetdiaghelpe_getcachetime.htm
tech.root: NDF
ms.assetid: 0298bf84-374e-438f-8141-3298e1004c1b
ms.date: 12/05/2018
ms.keywords: GetCacheTime, GetCacheTime method [NDF], GetCacheTime method [NDF],INetDiagHelper interface, INetDiagHelper interface [NDF],GetCacheTime method, INetDiagHelper.GetCacheTime, INetDiagHelper::GetCacheTime, ndf.inetdiaghelpe_getcachetime, ndhelper/INetDiagHelper::GetCacheTime
req.header: ndhelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetDiagHelper::GetCacheTime
 - ndhelper/INetDiagHelper::GetCacheTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ndhelper.h
api_name:
 - INetDiagHelper.GetCacheTime
---

# INetDiagHelper::GetCacheTime


## -description

The <b>GetCacheTime</b> method specifies the time when cached results of a diagnosis and repair operation have expired.

## -parameters

### -param pCacheTime [out]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.

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
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to complete this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters has not been provided correctly.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This optional method is not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient privileges to perform the diagnosis or repair operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The diagnosis or repair operation has been canceled.

</td>
</tr>
</table>
 

Helper Class Extensions may return HRESULTS that are specific to the failures encountered in the function.

## -remarks

This method is not required when building a Helper Class Extension.

The default behavior is to return the current time so that the results will not be cached.  Setting a cache time can increase diagnosis efficiency since NDF will not call on the extension to re-diagnose an issue unless the cache time has expired.

The <b>FILETIME</b> structure is a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (UTC).

## -see-also

<a href="/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper">INetDiagHelper</a>