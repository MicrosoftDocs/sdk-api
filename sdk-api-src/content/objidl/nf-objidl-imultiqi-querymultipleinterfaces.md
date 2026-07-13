---
UID: NF:objidl.IMultiQI.QueryMultipleInterfaces
title: IMultiQI::QueryMultipleInterfaces (objidl.h)
description: The IMultiQI::QueryMultipleInterfaces method (objidl.h) retrieves pointers to multiple supported interfaces on an object.
helpviewer_keywords: ["IMultiQI interface [COM]","QueryMultipleInterfaces method","IMultiQI.QueryMultipleInterfaces","IMultiQI::QueryMultipleInterfaces","QueryMultipleInterfaces","QueryMultipleInterfaces method [COM]","QueryMultipleInterfaces method [COM]","IMultiQI interface","_com_imultiqi_querymultipleinterfaces","com.imultiqi_querymultipleinterfaces","objidlbase/IMultiQI::QueryMultipleInterfaces"]
old-location: com\imultiqi_querymultipleinterfaces.htm
tech.root: com
ms.assetid: 412f1d03-f40c-4451-9c99-1134c69c9989
ms.date: 08/12/2022
ms.keywords: IMultiQI interface [COM],QueryMultipleInterfaces method, IMultiQI.QueryMultipleInterfaces, IMultiQI::QueryMultipleInterfaces, QueryMultipleInterfaces, QueryMultipleInterfaces method [COM], QueryMultipleInterfaces method [COM],IMultiQI interface, _com_imultiqi_querymultipleinterfaces, com.imultiqi_querymultipleinterfaces, objidlbase/IMultiQI::QueryMultipleInterfaces
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
 - IMultiQI::QueryMultipleInterfaces
 - objidl/IMultiQI::QueryMultipleInterfaces
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
 - IMultiQI.QueryMultipleInterfaces
---

# IMultiQI::QueryMultipleInterfaces


## -description

Retrieves pointers to multiple supported interfaces on an object.

Calling this method is equivalent to issuing a series of separate <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> calls except that you do not incur the overhead of a corresponding number of RPC calls. In multithreaded applications and distributed environments, keeping RPC calls to a minimum is essential for optimal performance.

## -parameters

### -param cMQIs [in]

The number of elements in the <i>pMQIs</i> array.

### -param pMQIs [in, out]

An array of <a href="/windows/desktop/api/objidl/ns-objidl-multi_qi">MULTI_QI</a> structures. For more information, see Remarks.

## -returns

This method can return the following values.

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
The method retrieved pointers to all requested interfaces.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method retrieved pointers to some, but not all, of the requested interfaces.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The method retrieved pointers to none of the requested interfaces.

</td>
</tr>
</table>

## -remarks

The <b>QueryMultipleInterfaces</b> method takes as input an array of <a href="/windows/desktop/api/objidl/ns-objidl-multi_qi">MULTI_QI</a> structures. Each structure specifies an interface IID and contains two additional members for receiving an interface pointer and return value.

This method obtains as many requested interface pointers as possible directly from the object proxy. For each interface not implemented on the proxy, the method calls the server to obtain a pointer. Upon receiving an interface pointer from the server, the method builds a corresponding interface proxy and returns its pointer along with pointers to the interfaces it already implements.


<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A caller should begin by querying the object proxy for the <a href="/windows/desktop/api/objidl/nn-objidl-imultiqi">IMultiQI</a> interface. If the object proxy returns a pointer to this interface, the caller should then create a <a href="/windows/desktop/api/objidl/ns-objidl-multi_qi">MULTI_QI</a> structure for each interface it wants to obtain. Each structure should specify an interface IID and set its <b>pItf</b> member to <b>NULL</b>. Failure to set the <b>pItf</b> member to <b>NULL</b> will cause the object proxy to ignore the structure.

On return, <b>QueryMultipleInterfaces</b> writes the requested interface pointer and a return value into each <a href="/windows/desktop/api/objidl/ns-objidl-multi_qi">MULTI_QI</a> structure in the client's array. The <b>pItf</b> member receives the pointer; the <b>hr</b> member receives the return value.

If the value returned from a call to <b>QueryMultipleInterfaces</b> is S_OK, then pointers were returned for all requested interfaces.

If the return value is E_NOINTERFACE, then pointers were returned for none of the requested interfaces. If the return value is S_FALSE, then pointers to one or more requested interfaces were not returned. In this event, the client should check the <b>hr</b> member of each <a href="/windows/desktop/api/objidl/ns-objidl-multi_qi">MULTI_QI</a> structure to determine which interfaces were acquired and which were not.

If a client knows ahead of time that it will be using several of an object's interfaces, it can call <b>QueryMultipleInterfaces</b> up front and then, later, if a <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> is done for one of the interfaces already acquired through <b>QueryMultipleInterfaces</b>, no RPC call will be necessary.



On return, the caller should check the <b>hr</b> member of each <a href="/windows/desktop/api/objidl/ns-objidl-multi_qi">MULTI_QI</a> structure to determine which interface pointers were and were not returned.

The client is responsible for releasing each of the acquired interfaces by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imultiqi">IMultiQI</a>
