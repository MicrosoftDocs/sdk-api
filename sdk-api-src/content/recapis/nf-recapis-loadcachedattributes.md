---
UID: NF:recapis.LoadCachedAttributes
title: LoadCachedAttributes function
author: windows-sdk-content
description: Loads the cached attributes of a recognizer.
old-location: tablet\loadcachedattributes.htm
tech.root: tablet
ms.assetid: 19DC01B8-FB2C-4724-907A-E68A9DD37FF3
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: LoadCachedAttributes, LoadCachedAttributes function [Tablet PC], recapis/LoadCachedAttributes, tablet.loadcachedattributes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - LoadCachedAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- LoadCachedAttributes
: 
---

# LoadCachedAttributes function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

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
 



