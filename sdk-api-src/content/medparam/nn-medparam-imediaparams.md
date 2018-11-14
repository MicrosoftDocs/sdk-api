---
UID: NN:medparam.IMediaParams
title: IMediaParams
author: windows-sdk-content
description: The IMediaParams interface sets and retrieves envelope-following parameters on an object.
old-location: dshow\imediaparams.htm
tech.root: DirectShow
ms.assetid: 68ea8f6a-4b6d-4d79-a986-6032b767147b
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IMediaParams, IMediaParams interface [DirectShow], IMediaParams interface [DirectShow],described, IMediaParamsInterface, dshow.imediaparams, medparam/IMediaParams
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: medparam.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaParams interface


## -description



The <code>IMediaParams</code> interface sets and retrieves envelope-following parameters on an object.



To reduce overhead, parameters are referenced by index value, and all parameter values are 32 bits, defined as type <b>MP_DATA</b>. Use the <a href="https://msdn.microsoft.com/80c7da71-7898-4bda-a181-09ad8906532a">IMediaParamInfo</a> interface to determine whether a given parameter is an integer, floating-point value, Boolean value, or member of an enumerated type.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaParams</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMediaParams</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaParams</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/acf7c96c-ce0c-40d0-b4a1-dd571fa2a514">AddEnvelope</a>
</td>
<td align="left" width="63%">
Adds an envelope to a parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/574d6573-ea5d-4419-ad65-f5f7d711e720">FlushEnvelope</a>
</td>
<td align="left" width="63%">
Flushes envelope data for a specified parameter over the specified time range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4fcae36a-c659-4565-9169-66d97beb26a4">GetParam</a>
</td>
<td align="left" width="63%">
Retrieves the most recent value of the specified parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e92681d4-2c77-4c72-b3ad-f0a6be7920e2">SetParam</a>
</td>
<td align="left" width="63%">
Sets the value of a parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48c28dd8-aeae-4212-9221-ab943113aa76">SetTimeFormat</a>
</td>
<td align="left" width="63%">
Specifies the time format for the object.

</td>
</tr>
</table> 

