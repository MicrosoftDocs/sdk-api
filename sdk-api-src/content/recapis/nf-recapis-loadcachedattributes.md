---
UID: NF:recapis.LoadCachedAttributes
title: LoadCachedAttributes function (recapis.h)
description: Loads the cached attributes of a recognizer.
helpviewer_keywords: ["LoadCachedAttributes","LoadCachedAttributes function [Tablet PC]","recapis/LoadCachedAttributes","tablet.loadcachedattributes"]
old-location: tablet\loadcachedattributes.htm
tech.root: tablet
ms.assetid: 19DC01B8-FB2C-4724-907A-E68A9DD37FF3
ms.date: 12/05/2018
ms.keywords: LoadCachedAttributes, LoadCachedAttributes function [Tablet PC], recapis/LoadCachedAttributes, tablet.loadcachedattributes
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
 - LoadCachedAttributes
 - recapis/LoadCachedAttributes
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
 - LoadCachedAttributes
---

# LoadCachedAttributes function


## -description



Loads the cached attributes of a recognizer.

## -parameters

### -param clsid

The CLSID of the recognizer. This value is created in the registry when you register the recognizer.

### -param pRecoAttributes

Pointer to the recognizer attributes.

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
The parameter is an invalid pointer.

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

