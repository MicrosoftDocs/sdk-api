---
UID: NF:oleidl.IOleItemContainer.GetObject
title: IOleItemContainer::GetObject (oleidl.h)
description: Retrieves a pointer to the specified object.
helpviewer_keywords: ["GetObject","GetObject method [COM]","GetObject method [COM]","IOleItemContainer interface","IOleItemContainer interface [COM]","GetObject method","IOleItemContainer.GetObject","IOleItemContainer::GetObject","_com_ioleitemcontainer_getobject","com.ioleitemcontainer_getobject","oleidl/IOleItemContainer::GetObject"]
old-location: com\ioleitemcontainer_getobject.htm
tech.root: com
ms.assetid: 08569037-7ecd-4e63-9f94-c2552c327800
ms.date: 12/05/2018
ms.keywords: GetObject, GetObject method [COM], GetObject method [COM],IOleItemContainer interface, IOleItemContainer interface [COM],GetObject method, IOleItemContainer.GetObject, IOleItemContainer::GetObject, _com_ioleitemcontainer_getobject, com.ioleitemcontainer_getobject, oleidl/IOleItemContainer::GetObject
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.idl
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
 - IOleItemContainer::GetObject
 - oleidl/IOleItemContainer::GetObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleItemContainer.GetObject
---

# IOleItemContainer::GetObject


## -description

Retrieves a pointer to the specified object.

## -parameters

### -param pszItem [in]

The container's name for the requested object.

### -param dwSpeedNeeded [in]

 Indicates approximately how long the caller will wait to get the object. Possible values are taken from the enumeration <a href="/windows/desktop/api/oleidl/ne-oleidl-bindspeed">BINDSPEED</a>.

### -param pbc [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on the bind context object to be used in this binding operation. The bind context caches objects bound during the binding process, contains parameters that apply to all operations using the bind context, and provides the means by which the binding implementation should retrieve information about its environment.

### -param riid [in]

A reference to the identifier of the interface pointer requested.

### -param ppvObject [out]

Address of the pointer variable that receives the interface pointer requested in <i>riid</i>. Upon successful return, *<i>ppvObject</i> contains the requested interface pointer to the object named by <i>pszItem</i>. When successful, the implementation must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the *<i>ppvObject</i>; it is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. If an error occurs, the implementation sets *<i>ppvObject</i> to <b>NULL</b>.

## -returns

This method can return the standard return value E_OUTOFMEMORY, as well as the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_EXCEEDEDDEADLINE</b></dt>
</dl>
</td>
<td width="60%">
The binding operation could not be completed within the time limit specified by the bind context's <a href="/windows/desktop/api/objidl/ns-objidl-bind_opts">BIND_OPTS</a> structure, or with the speed indicated by the <i>dwSpeedNeeded</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NOOBJECT</b></dt>
</dl>
</td>
<td width="60%">
The parameter <i>pszItem</i> does not identify an object in this container.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The requested interface was not available.

</td>
</tr>
</table>

## -remarks

The item moniker implementation of <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a> calls this method, passing the name stored within the item moniker as the <i>pszItem</i> parameter.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Your implementation of <b>IOleItemContainer::GetObject</b> should first determine whether <i>pszItem</i> is a valid name for one of the container's objects. If not, you should return MK_E_NOOBJECT.

If <i>pszItem</i> names an embedded or linked object, your implementation must check the value of the <i>dwSpeedNeeded</i> parameter. If the value is BINDSPEED_IMMEDIATE and the object is not yet loaded, you should return MK_E_EXCEEDEDDEADLINE. If the object is loaded, your implementation should determine whether the object is running (for example, by calling the <a href="/windows/desktop/api/ole2/nf-ole2-oleisrunning">OleIsRunning</a> function). If it is not running and the <i>dwSpeedNeeded</i> value is BINDSPEED_MODERATE, your implementation should return MK_E_EXCEEDEDDEADLINE. If the object is not running and <i>dwSpeedNeeded</i> is BINDSPEED_INDEFINITE, your implementation should call the <a href="/windows/desktop/api/ole2/nf-ole2-olerun">OleRun</a> function to put the object in the running state. Then it can query the object for the requested interface. Note that it is important the object be running before you query for the interface.

If <i>pszItem</i> names a pseudo-object, your implementation can ignore the <i>dwSpeedNeeded</i> parameter because a pseudo-object is running whenever its container is running. In this case, your implementation can simply query for the requested interface.

If you need more specific information about the time limit than is given by <i>dwSpeedNeeded</i>, you can call <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getbindoptions">IBindCtx::GetBindOptions</a> on the <i>pbc</i> parameter to get the actual deadline parameter.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a>