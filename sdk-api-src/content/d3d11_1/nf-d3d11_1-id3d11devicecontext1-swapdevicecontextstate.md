---
UID: NF:d3d11_1.ID3D11DeviceContext1.SwapDeviceContextState
title: ID3D11DeviceContext1::SwapDeviceContextState (d3d11_1.h)
description: Activates the given context state object and changes the current device behavior to Direct3D 11, Direct3D 10.1, or Direct3D 10.
helpviewer_keywords: ["ID3D11DeviceContext1 interface [Direct3D 11]","SwapDeviceContextState method","ID3D11DeviceContext1.SwapDeviceContextState","ID3D11DeviceContext1::SwapDeviceContextState","SwapDeviceContextState","SwapDeviceContextState method [Direct3D 11]","SwapDeviceContextState method [Direct3D 11]","ID3D11DeviceContext1 interface","d3d11_1/ID3D11DeviceContext1::SwapDeviceContextState","direct3d11.id3d11devicecontext1_swapdevicecontextstate"]
old-location: direct3d11\id3d11devicecontext1_swapdevicecontextstate.htm
tech.root: direct3d11
ms.assetid: 4E267E86-602F-459C-A6F9-4660EC8FA752
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext1 interface [Direct3D 11],SwapDeviceContextState method, ID3D11DeviceContext1.SwapDeviceContextState, ID3D11DeviceContext1::SwapDeviceContextState, SwapDeviceContextState, SwapDeviceContextState method [Direct3D 11], SwapDeviceContextState method [Direct3D 11],ID3D11DeviceContext1 interface, d3d11_1/ID3D11DeviceContext1::SwapDeviceContextState, direct3d11.id3d11devicecontext1_swapdevicecontextstate
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext1::SwapDeviceContextState
 - d3d11_1/ID3D11DeviceContext1::SwapDeviceContextState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext1.SwapDeviceContextState
---

# ID3D11DeviceContext1::SwapDeviceContextState


## -description

Activates the given context state object and changes the current device behavior to Direct3D 11, Direct3D 10.1, or Direct3D 10.

## -parameters

### -param pState [in]

A pointer to the <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate">ID3DDeviceContextState</a> interface for the context state object that was previously created through the <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate">ID3D11Device1::CreateDeviceContextState</a> method. If <b>SwapDeviceContextState</b> is called with <i>pState</i> set to <b>NULL</b>, the call has no effect.

### -param ppPreviousState [out, optional]

A pointer to a variable that receives a pointer to the <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate">ID3DDeviceContextState</a> interface for the previously-activated context state object.

## -remarks

<b>SwapDeviceContextState</b> changes device behavior. This device behavior depends on the emulated interface that you passed to the <i>EmulatedInterface</i> parameter of the  <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate">ID3D11Device1::CreateDeviceContextState</a> method when you created the context state object. 

<b>SwapDeviceContextState</b> is not supported on a deferred context.

<b>SwapDeviceContextState</b> disables the incompatible device interfaces <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>, <a href="/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1">ID3D10Device1</a>, <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>, and <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1">ID3D11Device1</a>. When a context state object is active, the runtime disables certain methods on the device and context interfaces. A context state object that is created with <code>__uuidof(ID3D11Device1)</code> or <code>__uuidof(ID3D11Device)</code> turns off most of the Direct3D 10 device interfaces. A context state object that is created with <code>__uuidof(ID3D10Device1)</code> or <code>__uuidof(ID3D10Device)</code> turns off most of the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> methods.
For more information about this behavior, see <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate">ID3D11Device1::CreateDeviceContextState</a>.

<b>SwapDeviceContextState</b> activates the context state object specified by <i>pState</i>. This means that the device behaviors that are associated with the context state object's feature level and compatible interface are activated on the Direct3D device until the next call to <b>SwapDeviceContextState</b>. In addition, any state that was saved when this context state object was last active is now reactivated, so that the previous state is replaced.

<b>SwapDeviceContextState</b> sets <i>ppPreviousState</i> to the most recently activated context state object. The object allows the caller to save and then later restore the previous device state. This behavior is useful in a plug-in architecture such as Direct2D that shares a Direct3D device with its plug-ins. A Direct2D interface can use context state objects to save and restore the application's state.

If the caller did not previously call the <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate">ID3D11Device1::CreateDeviceContextState</a> method to create a previous context state object, <b>SwapDeviceContextState</b> sets <i>ppPreviousState</i> to the default context state object. In either case, usage of <b>SwapDeviceContextState</b> is the same.

The feature level that is specified by the application, and that is chosen by the context state object from the acceptable list that the application supplies to <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate">ID3D11Device1::CreateDeviceContextState</a>, controls the feature level of the immediate context whenever the context state object is active. Because the Direct3D 11 device is free-threaded, the device methods cannot query the current immediate context feature level. Instead, the device runs at a feature level that is the maximum of all previously created context state objects' feature levels. This means that the device's feature level can increase dynamically.

The feature level of the context state object controls the functionality available from the immediate context. However, to maintain the free-threaded contract of the Direct3D 11 device methods—the resource-creation methods in particular—the upper-bound feature level of all created context state objects controls the set of resources that the device creates.

Because the context state object interface is published by the immediate context, the interface requires the same threading model as the immediate context. Specifically, <b>SwapDeviceContextState</b> is single-threaded with respect to the other immediate context methods and with respect to the equivalent methods of <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>.

Crucially, because only one of the Direct3D 10 or Direct3D 11 ref-count behaviors can be available at a time, one of the Direct3D 10 and Direct3D 11 interfaces must break its ref-count contract. To avoid this situation, the activation of a context state object turns off the incompatible version interface. Also, if you call a method of an incompatible version interface, the call silently fails if the method has  return type <b>void</b>, returns an <b>HRESULT</b> value of <b>E_INVALIDARG</b>, or sets any out parameter to <b>NULL</b>.

When you switch from Direct3D 11 mode to either Direct3D 10 mode or Direct3D 10.1 mode, the binding behavior of the device changes. Specifically, the final release of a resource induces unbind in Direct3D 10 mode or Direct3D 10.1 mode. During final release an application releases all of the resource's references, including indirect references such as the linkage from view to resource, and the linkage from context state object to any of the context state object's bound resources. Any bound resource to which the application has no reference is unbound and destroyed, in order to maintain the Direct3D 10 behavior.

<b>SwapDeviceContextState</b> does not affect any state that <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a> sets. 

Command lists that are generated by deferred contexts do not hold a reference to context state objects and are not affected by future updates to context state objects.

No asynchronous objects are affected by <b>SwapDeviceContextState</b>. For example, if a query is active before a call to <b>SwapDeviceContextState</b>, it is still active after the call.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1">ID3D11DeviceContext1</a>