---
UID: NN:medparam.IMediaParams
title: IMediaParams (medparam.h)
author: windows-sdk-content
description: The IMediaParams interface sets and retrieves envelope-following parameters on an object.
old-location: dshow\imediaparams.htm
tech.root: DirectShow
ms.assetid: 68ea8f6a-4b6d-4d79-a986-6032b767147b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMediaParams, IMediaParams interface [DirectShow], IMediaParams interface [DirectShow],described, IMediaParamsInterface, dshow.imediaparams, medparam/IMediaParams
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



To reduce overhead, parameters are referenced by index value, and all parameter values are 32 bits, defined as type <b>MP_DATA</b>. Use the <a href="https://msdn.microsoft.com/en-us/library/Dd406964(v=VS.85).aspx">IMediaParamInfo</a> interface to determine whether a given parameter is an integer, floating-point value, Boolean value, or member of an enumerated type.


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
<a href="https://msdn.microsoft.com/en-us/library/Dd406972(v=VS.85).aspx">AddEnvelope</a>
</td>
<td align="left" width="63%">
Adds an envelope to a parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406973(v=VS.85).aspx">FlushEnvelope</a>
</td>
<td align="left" width="63%">
Flushes envelope data for a specified parameter over the specified time range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406974(v=VS.85).aspx">GetParam</a>
</td>
<td align="left" width="63%">
Retrieves the most recent value of the specified parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406975(v=VS.85).aspx">SetParam</a>
</td>
<td align="left" width="63%">
Sets the value of a parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406976(v=VS.85).aspx">SetTimeFormat</a>
</td>
<td align="left" width="63%">
Specifies the time format for the object.

</td>
</tr>
</table> 

