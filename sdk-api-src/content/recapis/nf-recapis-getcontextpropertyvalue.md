---
UID: NF:recapis.GetContextPropertyValue
title: GetContextPropertyValue function (recapis.h)
description: Returns a specified property value from the recognizer context.
helpviewer_keywords: ["GetContextPropertyValue","GetContextPropertyValue function [Tablet PC]","e3f154ce-b4bf-4520-a4de-03cfe27ef9b0","recapis/GetContextPropertyValue","tablet.getcontextpropertyvalue"]
old-location: tablet\getcontextpropertyvalue.htm
tech.root: tablet
ms.assetid: e3f154ce-b4bf-4520-a4de-03cfe27ef9b0
ms.date: 12/05/2018
ms.keywords: GetContextPropertyValue, GetContextPropertyValue function [Tablet PC], e3f154ce-b4bf-4520-a4de-03cfe27ef9b0, recapis/GetContextPropertyValue, tablet.getcontextpropertyvalue
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
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
req.lib: 
req.dll: inkobjcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetContextPropertyValue
 - recapis/GetContextPropertyValue
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
 - GetContextPropertyValue
---

# GetContextPropertyValue function


## -description

Returns a specified property value from the recognizer context.

## -parameters

### -param hrc

The handle to the recognizer context.

### -param pGuid

The property to retrieve. Specify a predefined property globally unique identifier (GUID) or application-defined GUID. For a list of predefined properties, see the recognition <a href="/windows/desktop/tablet/property-guids">Property GUIDs</a>.

### -param pcbSize

On input, the size, in bytes, the <i>pProperty </i> buffer can be. On output, the size, in bytes, the <i>pProperty</i> buffer is.

### -param pProperty

The user allocated buffer to contain the property value. To determine the size of the buffer, set <i>pProperty</i> to <b>NULL</b>; use the size to allocate <i>pProperty</i>.

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
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_UNINITIALIZED_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The property has not been set by the context. This may occur if the property is set only in certain circumstances, or if the property is to be set only after an event that has not yet occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_INVALID_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The recognizer does not support the property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pProperty</i> buffer is too small.

</td>
</tr>
</table>

## -remarks

This function is optional.

You can use the <b>GetContextPropertyValue</b> function to get information that the recognizer is returning to the caller. This enables a customized recognizer to have modes and settings, and to return data that is unique to that recognizer.

In the Microsoft recognizers, calling the <b>GetContextPropertyValue</b> function with the <i>pcbSize</i> parameter set to a value larger than required does not result in an incorrect return value. Instead, the code automatically changes the size to the required value for the current GUID.

## -see-also

<a href="/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist">GetContextPropertyList Function</a>



<a href="/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue">SetContextPropertyValue Function</a>