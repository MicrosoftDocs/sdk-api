---
UID: NF:oleauto.CreateErrorInfo
title: CreateErrorInfo function (oleauto.h)
description: Creates an instance of a generic error object.
helpviewer_keywords: ["CreateErrorInfo","CreateErrorInfo function [Automation]","_oa96_CreateErrorInfo","automat.createerrorinfo","oleauto/CreateErrorInfo"]
old-location: automat\createerrorinfo.htm
tech.root: automat
ms.assetid: 6a9dd862-754a-48e3-8be5-d1fbd1d38f2b
ms.date: 12/05/2018
ms.keywords: CreateErrorInfo, CreateErrorInfo function [Automation], _oa96_CreateErrorInfo, automat.createerrorinfo, oleauto/CreateErrorInfo
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
 - CreateErrorInfo
 - oleauto/CreateErrorInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-ole32-l1-1-0.dll
 - OleAut32.dll
 - API-MS-Win-Downlevel-OLE32-l1-1-1.dll
 - ComBase.dll
api_name:
 - CreateErrorInfo
---

# CreateErrorInfo function


## -description

Creates an instance of a generic error object.

## -parameters

### -param pperrinfo [out]

A system-implemented generic error object.

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
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Could not create the error object.

</td>
</tr>
</table>

## -remarks

This function returns a pointer to a generic error object, which you can use with <b>QueryInterface</b> on <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreateerrorinfo">ICreateErrorInfo</a> to set its contents. You can then pass the resulting object to <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-seterrorinfo">SetErrorInfo</a>. The generic error object implements both <b>ICreateErrorInfo</b> and <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo">IErrorInfo</a>.

## -see-also

<a href="/previous-versions/windows/desktop/automat/error-handling-api-functions">Error-Handling API Functions</a>