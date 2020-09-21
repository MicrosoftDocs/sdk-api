---
UID: NF:oaidl.ITypeChangeEvents.AfterTypeChange
title: ITypeChangeEvents::AfterTypeChange (oaidl.h)
description: Raised after a type has been changed.
helpviewer_keywords: ["AfterTypeChange","AfterTypeChange method [Automation]","AfterTypeChange method [Automation]","ITypeChangeEvents interface","CHANGEKIND_ADDMEMBER","CHANGEKIND_CHANGEFAILED","CHANGEKIND_DELETEMEMBER","CHANGEKIND_GENERAL","CHANGEKIND_INVALIDATE","CHANGEKIND_SETDOCUMENTATION","CHANGEKIND_SETNAMES","ITypeChangeEvents interface [Automation]","AfterTypeChange method","ITypeChangeEvents.AfterTypeChange","ITypeChangeEvents::AfterTypeChange","_oa96_ITypeChangeEvents_AfterTypeChange","automat.itypechangeevents_aftertypechange","oaidl/ITypeChangeEvents::AfterTypeChange"]
old-location: automat\itypechangeevents_aftertypechange.htm
tech.root: automat
ms.assetid: 902663be-4cdb-47e5-916a-004483d6758e
ms.date: 12/05/2018
ms.keywords: AfterTypeChange, AfterTypeChange method [Automation], AfterTypeChange method [Automation],ITypeChangeEvents interface, CHANGEKIND_ADDMEMBER, CHANGEKIND_CHANGEFAILED, CHANGEKIND_DELETEMEMBER, CHANGEKIND_GENERAL, CHANGEKIND_INVALIDATE, CHANGEKIND_SETDOCUMENTATION, CHANGEKIND_SETNAMES, ITypeChangeEvents interface [Automation],AfterTypeChange method, ITypeChangeEvents.AfterTypeChange, ITypeChangeEvents::AfterTypeChange, _oa96_ITypeChangeEvents_AfterTypeChange, automat.itypechangeevents_aftertypechange, oaidl/ITypeChangeEvents::AfterTypeChange
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
 - ITypeChangeEvents::AfterTypeChange
 - oaidl/ITypeChangeEvents::AfterTypeChange
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
 - ITypeChangeEvents.AfterTypeChange
---

# ITypeChangeEvents::AfterTypeChange


## -description

Raised after a type has been changed.

## -parameters

### -param changeKind [in]

The type of change.

<a id="CHANGEKIND_ADDMEMBER"></a>
<a id="changekind_addmember"></a>


#### CHANGEKIND_ADDMEMBER

<a id="CHANGEKIND_DELETEMEMBER"></a>
<a id="changekind_deletemember"></a>


#### CHANGEKIND_DELETEMEMBER

<a id="CHANGEKIND_SETNAMES"></a>
<a id="changekind_setnames"></a>


#### CHANGEKIND_SETNAMES

<a id="CHANGEKIND_SETDOCUMENTATION"></a>
<a id="changekind_setdocumentation"></a>


#### CHANGEKIND_SETDOCUMENTATION

<a id="CHANGEKIND_GENERAL"></a>
<a id="changekind_general"></a>


#### CHANGEKIND_GENERAL

<a id="CHANGEKIND_INVALIDATE"></a>
<a id="changekind_invalidate"></a>


#### CHANGEKIND_INVALIDATE

<a id="CHANGEKIND_CHANGEFAILED"></a>
<a id="changekind_changefailed"></a>


#### CHANGEKIND_CHANGEFAILED

### -param pTInfoAfter [in]

An object that implements the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a>, <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo2">ITypeInfo2</a>, <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo">ICreateTypeInfo</a>, or <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo2">ICreateTypeInfo2</a> interface and that contains the type information before the change was made. The client subscribes to this object to receive notifications about any changes.

### -param pStrName [in]

The name of the change. This value may be null.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.


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

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypechangeevents">ITypeChangeEvents</a>