---
UID: NN:objidlbase.IMarshal
title: IMarshal (objidlbase.h)
description: The IMarshal (objidlbase.h) interface enables a COM object to define and manage the marshaling of its interface pointers.
helpviewer_keywords: ["IMarshal","IMarshal interface [COM]","IMarshal interface [COM]","described","_com_imarshal","com.imarshal","objidlbase/IMarshal"]
old-location: com\imarshal.htm
tech.root: com
ms.assetid: e6f08949-f27d-4aba-adff-eaf9c356a928
ms.date: 08/15/2022
ms.keywords: IMarshal, IMarshal interface [COM], IMarshal interface [COM],described, _com_imarshal, com.imarshal, objidlbase/IMarshal
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMarshal
 - objidlbase/IMarshal
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
 - IMarshal
---

# IMarshal interface


## -description

Enables a COM object to define and manage the marshaling of its interface pointers.

## -inheritance

The <b>IMarshal</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMarshal</b> also has these types of members:

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
      <a href="/windows/desktop/api/objidl/nn-objidl-irpcchannelbuffer">IRpcChannelBuffer</a>, to which both interface proxies and 
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
      <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> and 
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
      <a href="/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a> stub in the server process and uses it to 
      marshal the first pointer back to the client. In the client process, COM loads the generic proxy for the class 
      factory object and calls its implementation of <b>IMarshal</b> to 
      unmarshal that first pointer. COM then creates the first interface proxy and hands it a pointer to the RPC 
      channel. Finally, COM returns the <b>IClassFactory</b> pointer 
      to the client, which uses it to call 
      <a href="/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance">IClassFactory::CreateInstance</a>, passing it 
      a reference to the interface.

Back in the server process, COM now creates a new instance of the object, along with a stub for the requested 
      interface. This stub marshals the interface pointer back to the client process, where another object proxy is 
      created, this time for the object itself. Also created is a proxy for the requested interface, a pointer to 
      which is returned to the client. With subsequent calls to other interfaces on the object, COM will load the 
      appropriate interface stubs and proxies as needed.

When a new interface proxy is created, COM hands it a pointer to the proxy manager's implementation of 
      <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, to which it delegates all 
      <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> calls. Each interface proxy 
      implements two interfaces of its own: the interface it represents and 
      <a href="/windows/desktop/api/objidl/nn-objidl-irpcproxybuffer">IRpcProxyBuffer</a>. The interface proxy exposes its own 
      interface directly to clients, which can obtain its pointer by calling 
      <b>QueryInterface</b> on the proxy manager. Only COM, 
      however, can call <b>IRpcProxyBuffer</b>, which is used to 
      connect and disconnect the proxy to the RPC channel. A client cannot query an interface proxy to obtain a 
      pointer to the <b>IRpcProxyBuffer</b> interface.

On the server side, each interface stub implements 
      <a href="/windows/desktop/api/objidl/nn-objidl-irpcstubbuffer">IRpcStubBuffer</a>. The server code acting as a stub manager 
      calls <a href="/windows/desktop/api/objidl/nf-objidl-irpcstubbuffer-connect">IRpcStubBuffer::Connect</a> and passes the 
      interface stub the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer of its object.

When an interface proxy receives a method invocation, it obtains a marshaling packet from its RPC channel 
      through a call to 
      <a href="/windows/desktop/api/objidl/nf-objidl-irpcchannelbuffer-getbuffer">IRpcChannelBuffer::GetBuffer</a>. The process 
      of marshaling the arguments will copy data into the buffer. When marshaling is complete, the interface proxy 
      invokes <a href="/windows/desktop/api/objidl/nf-objidl-irpcchannelbuffer-sendreceive">IRpcChannelBuffer::SendReceive</a> to 
      send the marshaled packet to the corresponding interface stub. When 
      <b>IRpcChannelBuffer::SendReceive</b> returns, 
      the buffer into which the arguments were marshaled will have been replaced by a new buffer containing the return 
      values marshaled from the interface stub. The interface proxy unmarshals the return values, invokes 
      <a href="/windows/desktop/api/objidl/nf-objidl-irpcchannelbuffer-freebuffer">IRpcChannelBuffer::FreeBuffer</a> to free the 
      buffer, and then returns the return values to the original caller of the method.

It is the implementation of 
      <a href="/windows/desktop/api/objidl/nf-objidl-irpcchannelbuffer-sendreceive">IRpcChannelBuffer::SendReceive</a> that 
      actually sends the request to the server process and that knows how to identify the server process and, within 
      that process, the object to which the request should be sent. The channel implementation also knows how to 
      forward the request on to the appropriate stub manager in that process. The interface stub unmarshals the 
      arguments from the provided buffer, invokes the indicated method on the server object, and marshals the return 
      values back into a new buffer allocated by a call to 
      <a href="/windows/desktop/api/objidl/nf-objidl-irpcchannelbuffer-getbuffer">IRpcChannelBuffer::GetBuffer</a>. The channel 
      then transmits the return data packet back to the interface proxy, which is still in the middle of 
      <b>IRpcChannelBuffer::SendReceive</b>, which 
      returns to the interface proxy.

A particular instance of an interface proxy can be used to service more than one interface, as long as the 
       following conditions are met:

<ul>
<li>The IIDs of the affected interfaces must be mapped to the appropriate 
       <a href="/windows/desktop/com/proxystubclsid">ProxyStubClsid</a> in the system registry.</li>
<li>The interface proxy must support calls to 
       <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> from one supported interface to 
       the other interfaces, as usual, as well as from <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> and 
       <a href="/windows/desktop/api/objidl/nn-objidl-irpcproxybuffer">IRpcProxyBuffer</a>.</li>
</ul>
A single instance of an interface stub can also service more than one interface, but only if that set of 
      interfaces has a strict single-inheritance relationship. This restriction exists because the stub can direct 
      method invocations to multiple interfaces only where it knows in advance which methods are implemented on which 
      interfaces.

At various times, proxies and stubs will have need to allocate or free memory. Interface proxies, for example, 
      will need to allocate memory in which to return out parameters to their caller. In this respect, interface 
      proxies and interface stubs are just normal COM components, in that they should use the standard task allocator. 
      (See <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc">CoGetMalloc</a>.)

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-istdmarshalinfo">IStdMarshalInfo</a>
