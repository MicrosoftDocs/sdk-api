---
UID: NF:ndhelper.INetDiagHelper.GetKeyAttributes
title: INetDiagHelper::GetKeyAttributes (ndhelper.h)
description: Retrieves the key attributes of the Helper Class Extension.
helpviewer_keywords: ["GetKeyAttributes","GetKeyAttributes method [NDF]","GetKeyAttributes method [NDF]","INetDiagHelper interface","INetDiagHelper interface [NDF]","GetKeyAttributes method","INetDiagHelper.GetKeyAttributes","INetDiagHelper::GetKeyAttributes","ndf.inetdiaghelpe_getkeyattributes","ndhelper/INetDiagHelper::GetKeyAttributes"]
old-location: ndf\inetdiaghelpe_getkeyattributes.htm
tech.root: NDF
ms.assetid: f9501450-a883-4941-a03f-ab735acca82f
ms.date: 12/05/2018
ms.keywords: GetKeyAttributes, GetKeyAttributes method [NDF], GetKeyAttributes method [NDF],INetDiagHelper interface, INetDiagHelper interface [NDF],GetKeyAttributes method, INetDiagHelper.GetKeyAttributes, INetDiagHelper::GetKeyAttributes, ndf.inetdiaghelpe_getkeyattributes, ndhelper/INetDiagHelper::GetKeyAttributes
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
 - INetDiagHelper::GetKeyAttributes
 - ndhelper/INetDiagHelper::GetKeyAttributes
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
 - INetDiagHelper.GetKeyAttributes
---

# INetDiagHelper::GetKeyAttributes


## -description

The <b>GetKeyAttributes</b> method retrieves the key attributes of the Helper Class Extension.

## -parameters

### -param pcelt [out]

A pointer to a count of elements in the <b>HELPER_ATTRIBUTE</b> array.

### -param pprgAttributes [out]

A pointer to an array of <a href="/windows/desktop/api/ndattrib/ns-ndattrib-helper_attribute">HELPER_ATTRIBUTE</a> structures.

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

## -see-also

<a href="/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper">INetDiagHelper</a>