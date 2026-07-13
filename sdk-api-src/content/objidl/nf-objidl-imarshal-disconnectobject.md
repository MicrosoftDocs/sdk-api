---
UID: NF:objidl.IMarshal.DisconnectObject
title: IMarshal::DisconnectObject (objidl.h)
description: The IMarshal::DisconnectObject method (objidl.h) releases all connections to an object prior to shutting down. 
helpviewer_keywords: ["DisconnectObject","DisconnectObject method [COM]","DisconnectObject method [COM]","IMarshal interface","IMarshal interface [COM]","DisconnectObject method","IMarshal.DisconnectObject","IMarshal::DisconnectObject","_com_imarshal_disconnectobject","com.imarshal_disconnectobject","objidlbase/IMarshal::DisconnectObject"]
old-location: com\imarshal_disconnectobject.htm
tech.root: com
ms.assetid: 1a087fe2-d1ad-4ed9-b6f2-12389656e384
ms.date: 08/12/2022
ms.keywords: DisconnectObject, DisconnectObject method [COM], DisconnectObject method [COM],IMarshal interface, IMarshal interface [COM],DisconnectObject method, IMarshal.DisconnectObject, IMarshal::DisconnectObject, _com_imarshal_disconnectobject, com.imarshal_disconnectobject, objidlbase/IMarshal::DisconnectObject
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMarshal::DisconnectObject
 - objidl/IMarshal::DisconnectObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IMarshal.DisconnectObject
---

# IMarshal::DisconnectObject


## -description

Releases all connections to an object. The object's server calls the object's implementation of this method prior to shutting down.

## -parameters

### -param dwReserved [in]

This parameter is reserved and must be 0.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.

## -remarks

This method is implemented on the object, not the proxy.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The usual case in which this method is called occurs when an end user forcibly closes a COM server that has one or more running objects that implement <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>. Prior to shutting down, the server calls the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-codisconnectobject">CoDisconnectObject</a> function to release external connections to all its running objects. For each object that implements <b>IMarshal</b>, however, this function calls <b>DisconnectObject</b> so that each object that manages its own marshaling can take steps to notify its proxy that it is about to shut down.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
As part of its normal shutdown code, a server should call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-codisconnectobject">CoDisconnectObject</a>, which in turn calls <b>DisconnectObject</b>, on each of its running objects that implements <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>.

The outcome of any implementation of this method should be to enable a proxy to respond to all subsequent calls from its client by returning RPC_E_DISCONNECTED or CO_E_OBJNOTCONNECTED rather than attempting to forward the calls on to the original object. It is up to the client to destroy the proxy.

If you are implementing this method for an immutable object, such as a moniker, your implementation does not need to do anything because such objects are typically copied whole into the client's address space. Therefore, they have neither a proxy nor a connection to the original object. For more information on marshaling immutable objects, see the "When to Implement" section of the <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> topic.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-codisconnectobject">CoDisconnectObject</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>
