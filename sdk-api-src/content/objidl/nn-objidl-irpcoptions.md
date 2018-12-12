---
UID: NN:objidl.IRpcOptions
title: IRpcOptions
author: windows-sdk-content
description: Enables callers to set or query the values of various properties that control how COM handles remote procedure calls (RPC).
old-location: com\irpcoptions.htm
tech.root: com
ms.assetid: aa5db8ac-4c29-43cf-a7ed-a870df9dfb82
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRpcOptions, IRpcOptions interface [COM], IRpcOptions interface [COM],described, _com_irpcoptions, com.irpcoptions, objidlbase/IRpcOptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - COM
api_location:
 - objidlbase.h
api_name:
 - IRpcOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRpcOptions interface


## -description


Enables callers to set or query the values of various properties that control how COM handles remote procedure calls (RPC).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRpcOptions</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IRpcOptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRpcOptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82f59cad-3718-4202-99d3-c3aafb8dbf56">Query</a>
</td>
<td align="left" width="63%">
Retrieves the value of an RPC binding option property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4412e45-adc7-47e4-a19c-9ada6407e6dc">Set</a>
</td>
<td align="left" width="63%">
Sets the value of an RPC binding option property.

</td>
</tr>
</table> 


## -remarks



Using this interface, callers can set or query the COMBND_RPCTIMEOUT property, which controls how long your machine will attempt to establish RPC communications with another before failing. The property can have any one of the values enumerated in the following table.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>RPC_C_BINDING_INFINITE_TIMEOUT
</td>
<td>Keep trying to establish communications with no timeout.
</td>
</tr>
<tr>
<td>RPC_C_BINDING_MIN_TIMEOUT
</td>
<td>Try to establish communications for the minimum time required by the protocol. This value favors performance over reliability.</td>
</tr>
<tr>
<td>RPC_C_BINDING_DEFAULT_TIMEOUT
</td>
<td>Try to establish communications for the default time. The value strikes a balance between performance and reliability.</td>
</tr>
<tr>
<td>RPC_C_BINDING_MAX_TIMEOUT
</td>
<td>Try to establish communications for the maximum time allowed by the protocol. This value favors reliability over performance.</td>
</tr>
</table>
 



