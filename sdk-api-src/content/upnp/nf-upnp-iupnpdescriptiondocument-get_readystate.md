---
UID: NF:upnp.IUPnPDescriptionDocument.get_ReadyState
title: IUPnPDescriptionDocument::get_ReadyState
author: windows-sdk-content
description: The ReadyState property specifies the status of the document load operation.
old-location: upnp\iupnpdescriptiondocument_readystate.htm
tech.root: UPnP
ms.assetid: 592939fa-ebce-419f-a813-ecbbe788fd8e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUPnPDescriptionDocument interface [UPnP APIs],get_ReadyState method, IUPnPDescriptionDocument.get_ReadyState, IUPnPDescriptionDocument::get_ReadyState, READYSTATE _COMPLETE, READYSTATE _INTERACTIVE, READYSTATE _LOADED, READYSTATE _LOADING, READYSTATE_UNINITIALIZED, _upnp_iupnpdescriptiondocument_readystate, get_ReadyState, get_ReadyState method [UPnP APIs], get_ReadyState method [UPnP APIs],IUPnPDescriptionDocument interface, upnp.iupnpdescriptiondocument_readystate, upnp/IUPnPDescriptionDocument::get_ReadyState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Upnp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDescriptionDocument.get_ReadyState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPDescriptionDocument::get_ReadyState


## -description


The 
<b>ReadyState</b> property specifies the status of the document load operation. This status indicates the state of the <a href="https://msdn.microsoft.com/02ae8af2-44f2-4b7c-a426-f2a26c43da37">IUPnPDescriptionDocument::Load</a> or <a href="https://msdn.microsoft.com/bfb1d833-13e8-4ffe-832d-f6640a42055a">IUPnPDescriptionDocument::LoadAsync</a> method. These states are the standard ready-state values for loading XML documents.


## -parameters




### -param plReadyState [out]

Receives a reference to the ready state. The values this parameter can receive are (in the order they are used by Universal Plug and Play): 



<table>
<tr>
<th>plReadyState Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="READYSTATE_UNINITIALIZED"></a><a id="readystate_uninitialized"></a><dl>
<dt><b>READYSTATE_UNINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The document object has been created.

</td>
</tr>
<tr>
<td width="40%"><a id="READYSTATE__LOADING"></a><a id="readystate__loading"></a><dl>
<dt><b>READYSTATE _LOADING</b></dt>
</dl>
</td>
<td width="60%">
The load operation has started.

</td>
</tr>
<tr>
<td width="40%"><a id="READYSTATE__COMPLETE"></a><a id="readystate__complete"></a><dl>
<dt><b>READYSTATE _COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The load operation is finished; the document has been downloaded and the XML has been parsed.

</td>
</tr>
<tr>
<td width="40%"><a id="READYSTATE__INTERACTIVE"></a><a id="readystate__interactive"></a><dl>
<dt><b>READYSTATE _INTERACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%"><a id="READYSTATE__LOADED"></a><a id="readystate__loaded"></a><dl>
<dt><b>READYSTATE _LOADED</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
</table>
 


## -returns



For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/25bd3abd-b270-4609-93bb-a786ccaa95dd">IUPnPDescriptionDocument</a>



<a href="https://msdn.microsoft.com/02ae8af2-44f2-4b7c-a426-f2a26c43da37">IUPnPDescriptionDocument::Load</a>



<a href="https://msdn.microsoft.com/bfb1d833-13e8-4ffe-832d-f6640a42055a">IUPnPDescriptionDocument::LoadAsync</a>
 

 

