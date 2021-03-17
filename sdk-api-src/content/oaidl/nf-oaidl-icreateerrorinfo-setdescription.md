---
UID: NF:oaidl.ICreateErrorInfo.SetDescription
title: ICreateErrorInfo::SetDescription (oaidl.h)
description: Sets the textual description of the error.
helpviewer_keywords: ["ICreateErrorInfo interface [Automation]","SetDescription method","ICreateErrorInfo.SetDescription","ICreateErrorInfo::SetDescription","SetDescription","SetDescription method [Automation]","SetDescription method [Automation]","ICreateErrorInfo interface","_oa96_ICreateErrorInfo_SetDescription","automat.icreateerrorinfo_setdescription","oaidl/ICreateErrorInfo::SetDescription"]
old-location: automat\icreateerrorinfo_setdescription.htm
tech.root: automat
ms.assetid: 32d10343-4be4-4ebc-b2fd-43a292c006b2
ms.date: 12/05/2018
ms.keywords: ICreateErrorInfo interface [Automation],SetDescription method, ICreateErrorInfo.SetDescription, ICreateErrorInfo::SetDescription, SetDescription, SetDescription method [Automation], SetDescription method [Automation],ICreateErrorInfo interface, _oa96_ICreateErrorInfo_SetDescription, automat.icreateerrorinfo_setdescription, oaidl/ICreateErrorInfo::SetDescription
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
 - ICreateErrorInfo::SetDescription
 - oaidl/ICreateErrorInfo::SetDescription
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
 - ICreateErrorInfo.SetDescription
---

# ICreateErrorInfo::SetDescription


## -description

Sets the textual description of the error.

## -parameters

### -param szDescription [in]

A brief description of the error.

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

The text should be supplied in the language specified by the locale ID (LCID) that was passed to the method raising the error. For more information, see LCID Attribute in <a href="/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language">Type Libraries and the Object Description Language</a>. 



Use of this function is demonstrated in the file Main.cpp of the COM Fundamentals Hello sample.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreateerrorinfo">ICreateErrorInfo</a>