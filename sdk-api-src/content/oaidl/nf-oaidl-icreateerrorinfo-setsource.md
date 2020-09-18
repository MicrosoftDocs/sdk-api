---
UID: NF:oaidl.ICreateErrorInfo.SetSource
title: ICreateErrorInfo::SetSource (oaidl.h)
description: Sets the language-dependent programmatic identifier (ProgID) for the class or application that raised the error.
helpviewer_keywords: ["ICreateErrorInfo interface [Automation]","SetSource method","ICreateErrorInfo.SetSource","ICreateErrorInfo::SetSource","SetSource","SetSource method [Automation]","SetSource method [Automation]","ICreateErrorInfo interface","_oa96_ICreateErrorInfo_SetSource","automat.icreateerrorinfo_setsource","oaidl/ICreateErrorInfo::SetSource"]
old-location: automat\icreateerrorinfo_setsource.htm
tech.root: automat
ms.assetid: 7f0e6349-9d31-4ab6-9a91-3822e81188e5
ms.date: 12/05/2018
ms.keywords: ICreateErrorInfo interface [Automation],SetSource method, ICreateErrorInfo.SetSource, ICreateErrorInfo::SetSource, SetSource, SetSource method [Automation], SetSource method [Automation],ICreateErrorInfo interface, _oa96_ICreateErrorInfo_SetSource, automat.icreateerrorinfo_setsource, oaidl/ICreateErrorInfo::SetSource
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
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
 - ICreateErrorInfo::SetSource
 - oaidl/ICreateErrorInfo::SetSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ICreateErrorInfo.SetSource
---

# ICreateErrorInfo::SetSource


## -description

Sets the language-dependent programmatic identifier (ProgID) for the class or application that raised the error.

## -parameters

### -param szSource [in]

A ProgID in the form <i>progname</i>.<i>objectname</i>.

## -returns

This method can return one of these values.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.


</td>
</tr>
</table>

## -remarks

This method should be used to identify the class or application that is the source of the error. The language for the returned ProgID depends on the locale identifier (LCID) that was passed to the method at the time of invocation.



Use of this function is demonstrated in the file Main.cpp of the COM Fundamentals Hello sample.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreateerrorinfo">ICreateErrorInfo</a>