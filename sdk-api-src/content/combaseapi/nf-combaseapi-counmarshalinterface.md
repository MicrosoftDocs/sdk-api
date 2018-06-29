---
UID: NF:combaseapi.CoUnmarshalInterface
title: CoUnmarshalInterface function
author: windows-sdk-content
description: Initializes a newly created proxy using data written into the stream by a previous call to the CoMarshalInterface function, and returns an interface pointer to that proxy.
old-location: com\counmarshalinterface.htm
old-project: com
ms.assetid: d0eac0da-2f41-40c4-b756-31bc22752c17
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: CoUnmarshalInterface, CoUnmarshalInterface function [COM], _com_CoUnmarshalInterface, com.counmarshalinterface, combaseapi/CoUnmarshalInterface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: REGCLS
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
 - CoUnmarshalInterface
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# CoUnmarshalInterface function


## -description


Initializes a newly created proxy using data written into the stream by a previous call to the <a href="https://msdn.microsoft.com/04ca1217-eac1-43e2-b736-8d7522ce8592">CoMarshalInterface</a> function, and returns an interface pointer to that proxy.


## -parameters




### -param pStm [in]

A pointer to the stream from which the interface is to be unmarshaled.


### -param riid [in]

A reference to the identifier of the interface to be unmarshaled. For <b>IID_NULL</b>, the returned interface is the one defined by the stream, objref.iid.


### -param ppv [out]

The address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppv</i> contains the requested interface pointer for the unmarshaled interface.


## -returns



This function can return the standard return value E_FAIL, errors returned by <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a>, and the following values.

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
The interface pointer was unmarshaled successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INVALIDPOINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pStm</i> is an invalid pointer.

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
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_OBJNOTCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The object application has been disconnected from the remoting system (for example, as a result of a call to the <a href="https://msdn.microsoft.com/4293316a-bafe-4fca-ad6a-68d8e99c8fba">CoDisconnectObject</a> function).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
An error occurred reading the registration database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The final <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> of this function for the requested interface returned E_NOINTERFACE.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Important</b>  <p class="note">Security Note: Calling this method with untrusted data is a security risk. Call this method only with trusted data. For more information, see <a href="http://go.microsoft.com/fwlink/?LinkId=798821">Untrusted Data Security Risks</a>.

</div>
<div> </div>
The <b>CoUnmarshalInterface</b> function performs the following tasks:

<ol>
<li>Reads from the stream the CLSID to be used to create an instance of the proxy.
</li>
<li>Gets an <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a> pointer to the proxy that is to do the unmarshaling. If the object uses COM's default marshaling implementation, the pointer thus obtained is to an instance of the generic proxy object. If the marshaling is occurring between two threads in the same process, the pointer is to an instance of the in-process free threaded marshaler. If the object provides its own marshaling code, <b>CoUnmarshalInterface</b> calls the <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> function, passing the CLSID it read from the marshaling stream. <b>CoCreateInstance</b> creates an instance of the object's proxy and returns an <b>IMarshal</b> interface pointer to the proxy.</li>
<li>Using whichever IMarshal interface pointer it has acquired, the function then calls <a href="https://msdn.microsoft.com/5b496028-57db-447e-8c5c-76b7ea0fa4ee">IMarshal::UnmarshalInterface</a> and, if appropriate, <a href="https://msdn.microsoft.com/c58c7768-9200-4370-930c-89a6c6d2b430">IMarshal::ReleaseMarshalData</a>. 
</li>
</ol>
The primary caller of this function is COM itself, from within interface proxies or stubs that unmarshal an interface pointer. There are, however, some situations in which you might call <b>CoUnmarshalInterface</b>. For example, if you are implementing a stub, your implementation would call <b>CoUnmarshalInterface</b> when the stub receives an interface pointer as a parameter in a method call.





## -see-also




<a href="https://msdn.microsoft.com/04ca1217-eac1-43e2-b736-8d7522ce8592">CoMarshalInterface</a>



<a href="https://msdn.microsoft.com/5b496028-57db-447e-8c5c-76b7ea0fa4ee">IMarshal::UnmarshalInterface</a>
 

 

