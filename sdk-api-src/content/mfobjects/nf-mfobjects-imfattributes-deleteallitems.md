---
UID: NF:mfobjects.IMFAttributes.DeleteAllItems
title: IMFAttributes::DeleteAllItems (mfobjects.h)
description: Removes all key/value pairs from the object's attribute list.
helpviewer_keywords: ["8d7ef03b-bb96-42bc-a1c3-49f8b0e499b8","DeleteAllItems","DeleteAllItems method [Media Foundation]","DeleteAllItems method [Media Foundation]","IMFAttributes interface","IMFAttributes interface [Media Foundation]","DeleteAllItems method","IMFAttributes.DeleteAllItems","IMFAttributes::DeleteAllItems","mf.imfattributes_deleteallitems","mfobjects/IMFAttributes::DeleteAllItems"]
old-location: mf\imfattributes_deleteallitems.htm
tech.root: mf
ms.assetid: 8d7ef03b-bb96-42bc-a1c3-49f8b0e499b8
ms.date: 12/05/2018
ms.keywords: 8d7ef03b-bb96-42bc-a1c3-49f8b0e499b8, DeleteAllItems, DeleteAllItems method [Media Foundation], DeleteAllItems method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],DeleteAllItems method, IMFAttributes.DeleteAllItems, IMFAttributes::DeleteAllItems, mf.imfattributes_deleteallitems, mfobjects/IMFAttributes::DeleteAllItems
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
 - IMFAttributes::DeleteAllItems
 - mfobjects/IMFAttributes::DeleteAllItems
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
 - IMFAttributes.DeleteAllItems
---

# IMFAttributes::DeleteAllItems


## -description

Removes all key/value pairs from the object's attribute list.



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

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>
