---
UID: NF:mfobjects.IMFAttributes.DeleteItem
title: IMFAttributes::DeleteItem (mfobjects.h)
description: Removes a key/value pair from the object's attribute list.
helpviewer_keywords: ["DeleteItem","DeleteItem method [Media Foundation]","DeleteItem method [Media Foundation]","IMFAttributes interface","IMFAttributes interface [Media Foundation]","DeleteItem method","IMFAttributes.DeleteItem","IMFAttributes::DeleteItem","ac72e6e4-f930-4de6-92a2-f15e5f9e5d74","mf.imfattributes_deleteitem","mfobjects/IMFAttributes::DeleteItem"]
old-location: mf\imfattributes_deleteitem.htm
tech.root: mf
ms.assetid: ac72e6e4-f930-4de6-92a2-f15e5f9e5d74
ms.date: 12/05/2018
ms.keywords: DeleteItem, DeleteItem method [Media Foundation], DeleteItem method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],DeleteItem method, IMFAttributes.DeleteItem, IMFAttributes::DeleteItem, ac72e6e4-f930-4de6-92a2-f15e5f9e5d74, mf.imfattributes_deleteitem, mfobjects/IMFAttributes::DeleteItem
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFAttributes::DeleteItem
 - mfobjects/IMFAttributes::DeleteItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAttributes.DeleteItem
---

# IMFAttributes::DeleteItem


## -description

Removes a key/value pair from the object's attribute list.

## -parameters

### -param guidKey [in]

GUID that identifies the value to delete.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

If the specified key does not exist, the method returns <b>S_OK</b>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>