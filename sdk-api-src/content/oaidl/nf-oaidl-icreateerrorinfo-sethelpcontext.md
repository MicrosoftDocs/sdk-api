---
UID: NF:oaidl.ICreateErrorInfo.SetHelpContext
title: ICreateErrorInfo::SetHelpContext (oaidl.h)
description: Sets the Help context identifier (ID) for the error.
helpviewer_keywords: ["ICreateErrorInfo interface [Automation]","SetHelpContext method","ICreateErrorInfo.SetHelpContext","ICreateErrorInfo::SetHelpContext","SetHelpContext","SetHelpContext method [Automation]","SetHelpContext method [Automation]","ICreateErrorInfo interface","_oa96_ICreateErrorInfo_SetHelpContext","automat.icreateerrorinfo_sethelpcontext","oaidl/ICreateErrorInfo::SetHelpContext"]
old-location: automat\icreateerrorinfo_sethelpcontext.htm
tech.root: automat
ms.assetid: 5c65f4bd-21ad-4118-bbe8-e2ff65b96213
ms.date: 12/05/2018
ms.keywords: ICreateErrorInfo interface [Automation],SetHelpContext method, ICreateErrorInfo.SetHelpContext, ICreateErrorInfo::SetHelpContext, SetHelpContext, SetHelpContext method [Automation], SetHelpContext method [Automation],ICreateErrorInfo interface, _oa96_ICreateErrorInfo_SetHelpContext, automat.icreateerrorinfo_sethelpcontext, oaidl/ICreateErrorInfo::SetHelpContext
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
 - ICreateErrorInfo::SetHelpContext
 - oaidl/ICreateErrorInfo::SetHelpContext
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
 - ICreateErrorInfo.SetHelpContext
---

# ICreateErrorInfo::SetHelpContext


## -description

Sets the Help context identifier (ID) for the error.

## -parameters

### -param dwHelpContext [in]

The Help context ID for the error.

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

This method sets the Help context ID for the error. To establish the Help file to which it applies, use <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreateerrorinfo-sethelpfile">ICreateErrorInfo::SetHelpFile</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreateerrorinfo">ICreateErrorInfo</a>