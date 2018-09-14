---
UID: NF:combaseapi.CoMarshalInterface
title: CoMarshalInterface function
author: windows-sdk-content
description: Writes into a stream the data required to initialize a proxy object in some client process.
old-location: com\comarshalinterface.htm
tech.root: com
ms.assetid: 04ca1217-eac1-43e2-b736-8d7522ce8592
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: CoMarshalInterface, CoMarshalInterface function [COM], _com_CoMarshalInterface, com.comarshalinterface, combaseapi/CoMarshalInterface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoMarshalInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoMarshalInterface function


## -description


Writes into a stream the data required to initialize a proxy object in some client process.


## -parameters




### -param pStm [in]

A pointer to the stream to be used during marshaling. See <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>.


### -param riid [in]

A reference to the identifier of the interface to be marshaled. This interface must be derived from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.


### -param pUnk [in]

A pointer to the interface to be marshaled. This interface must be derived from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.


### -param dwDestContext [in]

The destination context where the specified interface is to be unmarshaled. The possible values come from the enumeration <a href="https://msdn.microsoft.com/d7d09ab2-96e7-48da-9292-0e4ca6cebe64">MSHCTX</a>. Currently, unmarshaling can occur in another apartment of the current process (MSHCTX_INPROC), in another process on the same computer as the current process (MSHCTX_LOCAL), or in a process on a different computer (MSHCTX_DIFFERENTMACHINE).


### -param pvDestContext [in, optional]

This parameter is reserved and must be <b>NULL</b>.


### -param mshlflags [in]

The flags that specify whether the data to be marshaled is to be transmitted back to the client process (the typical  case) or written to a global table, where it can be retrieved by multiple clients. The possibles values come from the <a href="https://msdn.microsoft.com/42a482be-d4b8-4f2e-ae43-1d210cb44c7c">MSHLFLAGS</a> enumeration.


## -returns



This function can return the standard return values E_FAIL, E_OUTOFMEMORY, and E_UNEXPECTED, the stream-access error values returned by <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>, as well as the following values.

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
The <b>HRESULT</b> was marshaled successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a> or <a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize</a> function was not called on the current thread before this function was called.

</td>
</tr>
</table>
 




## -remarks



The <b>CoMarshalInterface</b> function marshals the interface referred to by riid on the object whose <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> implementation is pointed to by <i>pUnk</i>. To do so, the <b>CoMarshalInterface</b> function performs the following tasks:

<ol>
<li>
Queries the object for a pointer to the <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a> interface. If the object does not implement <b>IMarshal</b>, meaning that it relies on COM to provide marshaling support, <b>CoMarshalInterface</b> gets a pointer to COM's default implementation of <b>IMarshal</b>.

</li>
<li>
Gets the CLSID of the object's proxy by calling <a href="https://msdn.microsoft.com/900a0f19-dcd5-4135-bab8-c191ec7e95e4">IMarshal::GetUnmarshalClass</a>, using whichever <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a> interface pointer has been returned.

</li>
<li>
Writes the CLSID of the proxy to the stream to be used for marshaling.

</li>
<li>
Marshals the interface pointer by calling <a href="https://msdn.microsoft.com/c48a7123-bd00-4ff3-8880-7fc4b99e4299">IMarshal::MarshalInterface</a>.

</li>
</ol>
The COM library in the client process calls the <a href="https://msdn.microsoft.com/d0eac0da-2f41-40c4-b756-31bc22752c17">CoUnmarshalInterface</a> function to extract the data and initialize the proxy. Before calling <b>CoUnmarshalInterface</b>, seek back to the original position in the stream.

If you are implementing existing COM interfaces or defining your own interfaces using the Microsoft Interface Definition Language (MIDL), the MIDL-generated proxies and stubs call <b>CoMarshalInterface</b> for you. If you are writing your own proxies and stubs, your proxy code and stub code should each call <b>CoMarshalInterface</b> to correctly marshal interface pointers. Calling <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a> directly from your proxy and stub code is not recommended.

If you are writing your own implementation of <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a>, and your proxy needs access to a private object, you can include an interface pointer to that object as part of the data you write to the stream. In such situations, if you want to use COM's default marshaling implementation when passing the interface pointer, you can call <b>CoMarshalInterface</b> on the object to do so.





## -see-also




<a href="https://msdn.microsoft.com/d0eac0da-2f41-40c4-b756-31bc22752c17">CoUnmarshalInterface</a>



<a href="https://msdn.microsoft.com/c48a7123-bd00-4ff3-8880-7fc4b99e4299">IMarshal::MarshalInterface</a>
 

 

