---
UID: NF:recapis.GetContextPropertyList
title: GetContextPropertyList function (recapis.h)
description: Retrieves a list of properties the recognizer supports.
helpviewer_keywords: ["3d3df56f-d989-4d3b-a0e2-00a7ac0fabd6","GetContextPropertyList","GetContextPropertyList function [Tablet PC]","recapis/GetContextPropertyList","tablet.getcontextpropertylist"]
old-location: tablet\getcontextpropertylist.htm
tech.root: tablet
ms.assetid: 3d3df56f-d989-4d3b-a0e2-00a7ac0fabd6
ms.date: 12/05/2018
ms.keywords: 3d3df56f-d989-4d3b-a0e2-00a7ac0fabd6, GetContextPropertyList, GetContextPropertyList function [Tablet PC], recapis/GetContextPropertyList, tablet.getcontextpropertylist
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
 - GetContextPropertyList
 - recapis/GetContextPropertyList
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
 - GetContextPropertyList
---

# GetContextPropertyList function


## -description

Retrieves a list of properties the recognizer supports.

## -parameters

### -param hrc

The handle to the recognizer context.

### -param pcProperties

On input, the size, in bytes, the <i>pPropertyGUIDS</i> buffer can be. On output, the size, in bytes, the <i>pPropertyGUIDS</i> buffer is.

### -param pPropertyGUIDS

The user-allocated buffer to contain a list of properties the recognizer supports. To determine the size of the buffer, set <i>pPropertyGUIDS</i> to <b>NULL</b>; use the size (<i>pcProperties</i>) to allocate <i>pPropertyGUIDS</i>. For a list of predefined properties, see the recognition <a href="/windows/desktop/tablet/property-guids">Property GUIDs</a>.

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
<dt><b>TPC_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppPropertyGUIDS</i> buffer is too small.

</td>
</tr>
</table>

## -remarks

This function is optional.

When Microsoft recognition engines are called with the <i>pcProperties</i> parameter set to a value larger than the required value, it does not result in an error. Instead, the engine automatically changes the size to the required value for the recognizer.

## -see-also

<a href="/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue">GetContextPropertyValue Function</a>



<a href="/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue">SetContextPropertyValue Function</a>