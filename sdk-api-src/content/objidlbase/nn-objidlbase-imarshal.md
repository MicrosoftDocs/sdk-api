---
UID: NN:objidlbase.IMarshal
title: IMarshal
author: windows-sdk-content
description: Enables a COM object to define and manage the marshaling of its interface pointers.
old-location: com\imarshal.htm
tech.root: com
ms.assetid: e6f08949-f27d-4aba-adff-eaf9c356a928
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IMarshal, IMarshal interface [COM], IMarshal interface [COM],described, _com_imarshal, com.imarshal, objidlbase/IMarshal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidlbase.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IMarshal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMarshal interface


## -description


Enables a COM object to define and manage the marshaling of its interface pointers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMarshal</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IMarshal</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMarshal</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a087fe2-d1ad-4ed9-b6f2-12389656e384">DisconnectObject</a>
</td>
<td align="left" width="63%">
Releases all connections to an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25ec060a-ec46-4857-8d66-8f8bb58d6d31">GetMarshalSizeMax</a>
</td>
<td align="left" width="63%">
Retrieves the maximum size of the buffer that will be needed during marshaling.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/900a0f19-dcd5-4135-bab8-c191ec7e95e4">GetUnmarshalClass</a>
</td>
<td align="left" width="63%">
Retrieves the <b>CLSID</b> of the unmarshaling code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c48a7123-bd00-4ff3-8880-7fc4b99e4299">MarshalInterface</a>
</td>
<td align="left" width="63%">
Marshals an interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c58c7768-9200-4370-930c-89a6c6d2b430">ReleaseMarshalData</a>
</td>
<td align="left" width="63%">
Destroys a marshaled data packet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b496028-57db-447e-8c5c-76b7ea0fa4ee">UnmarshalInterface</a>
</td>
<td align="left" width="63%">
Unmarshals an interface pointer.

</td>
</tr>
</table> 


## -remarks



<i>Marshaling</i> is the process of packaging data into packets for transmission to a different process 
     or computer. Unmarshaling is the process of recovering that data at the receiving end. In any given call, method 
     arguments are marshaled and unmarshaled in one direction, while return values are marshaled and unmarshaled in 
     the other.

Although marshaling applies to all data types, interface pointers require special handling. The fundamental 
     problem is how client code running in one address space can correctly dereference a pointer to an interface on an 
     object residing in a different address space. The COM solution is for a client application to communicate with 
     the original object through a surrogate object, or proxy, which lives in the client's process. The proxy holds a 
     reference to an interface on the original object and hands the client a pointer to an interface on itself. When 
     the client calls an interface method on the original object, its call is actually going to the proxy. Therefore, 
     from the client's point of view, all calls are in-process.

On receiving a call, the proxy marshals the method arguments and through some means of interprocess 
     communication, such as RPC, passes them along to code in the server process, which unmarshals the arguments and 
     passes them to the original object. This same code marshals return values for transmission back to the proxy, 
     which unmarshals the values and passes them to the client application.

<b>IMarshal</b> provides methods for creating, initializing, and 
     managing a proxy in a client process; it does not dictate how the proxy should communicate with the original 
     object. The COM default implementation of <b>IMarshal</b> uses RPC. 
     When you implement this interface yourself, you are free to choose any method of interprocess communication you 
     deem to be appropriate for your application—shared memory, named pipe, window handle, 
     RPC—in short, whatever works.

<h3><a id="IMarshal_Default_Implementation"></a><a id="imarshal_default_implementation"></a><a id="IMARSHAL_DEFAULT_IMPLEMENTATION"></a>IMarshal Default Implementation</h3>
COM uses its own internal implementation of the <b>IMarshal</b> 
      interface to marshal any object that does not provide its own implementation. COM makes this determination by 
      querying the object for <b>IMarshal</b>. If the interface is 
      missing, COM defaults to its internal implementation.

The COM default implementation of <b>IMarshal</b> uses a generic 
      proxy for each object and creates individual stubs and proxies, as they are needed, for each interface 
      implemented on the object. This mechanism is necessary because COM cannot know in advance what particular 
      interfaces a given object may implement. Developers who do not use COM default marshaling, electing instead to 
      write their own proxy and marshaling routines, know at compile time all the interfaces to be found on their 
      objects and therefore understand exactly what marshaling code is required. COM, in providing marshaling support 
      for all objects, must do so at run time.

The <i>interface proxy</i> resides in the client process; the <i>interface stub</i> resides in the 
      server. Together, each pair handles all marshaling for the interface. The job of each interface proxy is to 
      marshal arguments and unmarshal return values and out parameters that are passed back and forth in subsequent 
      calls to its interface. The job of each interface stub is to unmarshal function arguments and pass them along to 
      the original object and then marshal the return values and out parameters that the object returns.

Proxy and stub communicate by means of an RPC (remote procedure call) channel, which utilizes the system's RPC 
      infrastructure for interprocess communication. The RPC channel implements a single interface, 
      <a href="https://msdn.microsoft.com/1d7d7e1c-a491-4625-97ae-0d4dc5d2fc20">IRpcChannelBuffer</a>, to which both interface proxies and 
      stubs hold a pointer. The proxy and stub call the interface to obtain a marshaling packet, send the data to 
      their counterpart, and destroy the packet when they are done. The interface stub also holds a pointer to the 
      original object.

For any given interface, the proxy and stub are both implemented as instances of the same class, which is 
      listed for each interface in the system registry under the label 
      <b>ProxyStubClsid32</b>. This entry maps the interface's IID to the 
      <b>CLSID</b> of its proxy and stub objects. When COM needs to marshal an interface, it 
      looks in the system registry to obtain the appropriate <b>CLSID</b>. The server 
      identified by this <b>CLSID</b> implements both the interface proxy and interface stub.

Most often, the class to which this <b>CLSID</b> refers is automatically generated by a 
      tool whose input is a description of the function signatures and semantics of a given interface, written in some 
      interface description language. While using such a language is highly recommended and encouraged for accuracy's 
      sake, doing so is not required. Proxies and stubs are merely COM components used by the RPC infrastructure and, 
      as such, can be written in any manner desired, as long as the correct external contracts are upheld. The 
      programmer who designs a new interface is responsible for ensuring that all interface proxies and stubs that 
      ever exist agree on the representation of their marshaled data.

When created, interface proxies are always aggregated into a larger proxy, which represents the object as a 
      whole. This object proxy also aggregates the COM generic proxy object, which is known as the 
      <i>proxy manager</i>. The proxy manager implements two interfaces: 
      <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> and 
      <b>IMarshal</b>. All of the other interfaces that may be implemented 
      on an object are exposed in its object proxy through the aggregation of individual interface proxies. A client 
      holding a pointer to the object proxy "believes" it holds a pointer to the actual object.

A proxy representing the object as a whole is required in the client process so that a client can distinguish 
      calls to the same interfaces implemented on entirely different objects. Such a requirement does not exist in the 
      server process, however, where the object itself resides, because all interface stubs communicate only with the 
      objects for which they were created. No other connection is possible.

Interface stubs, by contrast with interface proxies, are not aggregated because there is no need that they 
      appear to some external client to be part of a larger whole. When connected, an interface stub is given a 
      pointer to the server object to which it should forward method invocations that it receives. Although it is 
      useful to refer conceptually to a stub manager, meaning whatever pieces of code and state in the server-side RPC 
      infrastructure that service the remoting of a given object, there is no direct requirement that the code and 
      state take any particular, well-specified form.

The first time a client requests a pointer to an interface on a particular object, COM loads an 
      <a href="https://msdn.microsoft.com/f624f833-2b69-43bc-92cd-c4ecbe6051c5">IClassFactory</a> stub in the server process and uses it to 
      marshal the first pointer back to the client. In the client process, COM loads the generic proxy for the class 
      factory object and calls its implementation of <b>IMarshal</b> to 
      unmarshal that first pointer. COM then creates the first interface proxy and hands it a pointer to the RPC 
      channel. Finally, COM returns the <b>IClassFactory</b> pointer 
      to the client, which uses it to call 
      <a href="https://msdn.microsoft.com/45d34150-9e0b-4a76-a784-c81434ec73b8">IClassFactory::CreateInstance</a>, passing it 
      a reference to the interface.

Back in the server process, COM now creates a new instance of the object, along with a stub for the requested 
      interface. This stub marshals the interface pointer back to the client process, where another object proxy is 
      created, this time for the object itself. Also created is a proxy for the requested interface, a pointer to 
      which is returned to the client. With subsequent calls to other interfaces on the object, COM will load the 
      appropriate interface stubs and proxies as needed.

When a new interface proxy is created, COM hands it a pointer to the proxy manager's implementation of 
      <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>, to which it delegates all 
      <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> calls. Each interface proxy 
      implements two interfaces of its own: the interface it represents and 
      <a href="https://msdn.microsoft.com/e1b18997-f99b-4611-8ba6-da28fd8df898">IRpcProxyBuffer</a>. The interface proxy exposes its own 
      interface directly to clients, which can obtain its pointer by calling 
      <b>QueryInterface</b> on the proxy manager. Only COM, 
      however, can call <b>IRpcProxyBuffer</b>, which is used to 
      connect and disconnect the proxy to the RPC channel. A client cannot query an interface proxy to obtain a 
      pointer to the <b>IRpcProxyBuffer</b> interface.

On the server side, each interface stub implements 
      <a href="https://msdn.microsoft.com/0aa724f0-6110-4ebf-a0c1-d309074a61d9">IRpcStubBuffer</a>. The server code acting as a stub manager 
      calls <a href="https://msdn.microsoft.com/0a452287-b674-4b51-9690-316beeab4482">IRpcStubBuffer::Connect</a> and passes the 
      interface stub the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer of its object.

When an interface proxy receives a method invocation, it obtains a marshaling packet from its RPC channel 
      through a call to 
      <a href="https://msdn.microsoft.com/775a15df-8bcf-4c1b-a8b9-5c7c03106c09">IRpcChannelBuffer::GetBuffer</a>. The process 
      of marshaling the arguments will copy data into the buffer. When marshaling is complete, the interface proxy 
      invokes <a href="https://msdn.microsoft.com/8a42fd06-252f-4c1b-bbdb-abc2e3887c46">IRpcChannelBuffer::SendReceive</a> to 
      send the marshaled packet to the corresponding interface stub. When 
      <b>IRpcChannelBuffer::SendReceive</b> returns, 
      the buffer into which the arguments were marshaled will have been replaced by a new buffer containing the return 
      values marshaled from the interface stub. The interface proxy unmarshals the return values, invokes 
      <a href="https://msdn.microsoft.com/bcdd4783-4a75-42d0-86a9-ab2605abbbe1">IRpcChannelBuffer::FreeBuffer</a> to free the 
      buffer, and then returns the return values to the original caller of the method.

It is the implementation of 
      <a href="https://msdn.microsoft.com/8a42fd06-252f-4c1b-bbdb-abc2e3887c46">IRpcChannelBuffer::SendReceive</a> that 
      actually sends the request to the server process and that knows how to identify the server process and, within 
      that process, the object to which the request should be sent. The channel implementation also knows how to 
      forward the request on to the appropriate stub manager in that process. The interface stub unmarshals the 
      arguments from the provided buffer, invokes the indicated method on the server object, and marshals the return 
      values back into a new buffer allocated by a call to 
      <a href="https://msdn.microsoft.com/775a15df-8bcf-4c1b-a8b9-5c7c03106c09">IRpcChannelBuffer::GetBuffer</a>. The channel 
      then transmits the return data packet back to the interface proxy, which is still in the middle of 
      <b>IRpcChannelBuffer::SendReceive</b>, which 
      returns to the interface proxy.

A particular instance of an interface proxy can be used to service more than one interface, as long as the 
       following conditions are met:

<ul>
<li>The IIDs of the affected interfaces must be mapped to the appropriate 
       <a href="https://msdn.microsoft.com/07e1e9de-e529-496c-b9f7-e7f799089f02">ProxyStubClsid</a> in the system registry.</li>
<li>The interface proxy must support calls to 
       <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> from one supported interface to 
       the other interfaces, as usual, as well as from <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> and 
       <a href="https://msdn.microsoft.com/e1b18997-f99b-4611-8ba6-da28fd8df898">IRpcProxyBuffer</a>.</li>
</ul>
A single instance of an interface stub can also service more than one interface, but only if that set of 
      interfaces has a strict single-inheritance relationship. This restriction exists because the stub can direct 
      method invocations to multiple interfaces only where it knows in advance which methods are implemented on which 
      interfaces.

At various times, proxies and stubs will have need to allocate or free memory. Interface proxies, for example, 
      will need to allocate memory in which to return out parameters to their caller. In this respect, interface 
      proxies and interface stubs are just normal COM components, in that they should use the standard task allocator. 
      (See <a href="https://msdn.microsoft.com/d1d09fbe-ca5c-4480-b807-3afcc043ccb9">CoGetMalloc</a>.)




## -see-also




<a href="https://msdn.microsoft.com/f034436f-e24e-4b99-9fb9-b0400d3ebb72">IStdMarshalInfo</a>
 

 

