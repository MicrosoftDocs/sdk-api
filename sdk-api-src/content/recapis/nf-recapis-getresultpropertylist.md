---
UID: NF:recapis.GetResultPropertyList
title: GetResultPropertyList function (recapis.h)
description: Retrieves a list of properties the recognizer can return for a result range.
helpviewer_keywords: ["GetResultPropertyList","GetResultPropertyList function [Tablet PC]","e6c4e802-c1dd-4ee9-b1d8-d1ad1ec19a65","recapis/GetResultPropertyList","tablet.getresultpropertylist"]
old-location: tablet\getresultpropertylist.htm
tech.root: tablet
ms.assetid: e6c4e802-c1dd-4ee9-b1d8-d1ad1ec19a65
ms.date: 12/05/2018
ms.keywords: GetResultPropertyList, GetResultPropertyList function [Tablet PC], e6c4e802-c1dd-4ee9-b1d8-d1ad1ec19a65, recapis/GetResultPropertyList, tablet.getresultpropertylist
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: inkobjcore.lib
req.dll: inkobjcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetResultPropertyList
 - recapis/GetResultPropertyList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - GetResultPropertyList
---

# GetResultPropertyList function


## -description

Retrieves a list of properties the recognizer can return for a result range.

## -parameters

### -param hrec

Handle to the recognizer.

### -param pPropertyCount

On input, the number of GUIDs the <i>pPropertyGuid</i> buffer can hold. On output, the number of GUIDs the <i>pPropertyGuid</i> buffer contains.

### -param pPropertyGuid

Array of properties the recognizer can return. The order of the array is arbitrary. For a list of predefined properties, see the recognition <a href="/windows/desktop/tablet/property-guids">Property GUIDs</a>. To determine the required size of the buffer, set <i>pPropertyGuid</i> to <b>NULL</b>; use the number of GUIDs to allocate the buffer.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pPropertyGuid</i> buffer is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
</table>