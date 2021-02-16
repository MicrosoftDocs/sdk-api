---
UID: NF:infotech.IITDatabase.GetObject
title: IITDatabase::GetObject (infotech.h)
description: Retrieves a specified IUnknown-based interface on the object identified by the dwObjInstance parameter.
helpviewer_keywords: ["GetObject","GetObject method [HTML Help Workshop]","GetObject method [HTML Help Workshop]","IITDatabase interface","IITDatabase interface [HTML Help Workshop]","GetObject method","IITDatabase.GetObject","IITDatabase::GetObject","htmlhelp.iitdatabase_getobject","infotech/IITDatabase::GetObject","refIITDatabaseGetObject"]
old-location: htmlhelp\iitdatabase_getobject.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitdatabasegetobject.htm
ms.date: 12/05/2018
ms.keywords: GetObject, GetObject method [HTML Help Workshop], GetObject method [HTML Help Workshop],IITDatabase interface, IITDatabase interface [HTML Help Workshop],GetObject method, IITDatabase.GetObject, IITDatabase::GetObject, htmlhelp.iitdatabase_getobject, infotech/IITDatabase::GetObject, refIITDatabaseGetObject
req.header: infotech.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IITDatabase::GetObject
 - infotech/IITDatabase::GetObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Infotech.h
api_name:
 - IITDatabase.GetObject
---

# IITDatabase::GetObject


## -description

Retrieves a specified <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>-based interface on the object identified by the <i>dwObjInstance</i> parameter.

## -parameters

### -param dwObjInstance [in]

Identifier for object.

### -param riid [in]

### -param ppvObj [out]

Interface ID requested.

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
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument was not valid.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTINIT</b></dt>
</dl>
</td>
<td width="60%">
The database has not been opened.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The memory required for internal structures could not be allocated.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/infotech/nn-infotech-iitdatabase">IITDatabase</a>