---
UID: NF:objidl.IMarshal.UnmarshalInterface
title: IMarshal::UnmarshalInterface
author: windows-sdk-content
description: Unmarshals an interface pointer.
old-location: com\imarshal_unmarshalinterface.htm
old-project: com
ms.assetid: 5b496028-57db-447e-8c5c-76b7ea0fa4ee
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IMarshal interface [COM],UnmarshalInterface method, IMarshal.UnmarshalInterface, IMarshal::UnmarshalInterface, UnmarshalInterface, UnmarshalInterface method [COM], UnmarshalInterface method [COM],IMarshal interface, _com_imarshal_unmarshalinterface, com.imarshal_unmarshalinterface, objidlbase/IMarshal::UnmarshalInterface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IMarshal.UnmarshalInterface
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMarshal::UnmarshalInterface


## -description


Unmarshals an interface pointer.


## -parameters




### -param pStm [in]

A pointer to the stream from which the interface pointer is to be unmarshaled.


### -param riid [in]

A reference to the identifier of the interface to be unmarshaled.


### -param ppv [out]

The address of pointer variable that receives the interface pointer. Upon successful return, *<i>ppv</i> contains the requested interface pointer of the interface to be unmarshaled.


## -returns



This method can return the standard return value E_FAIL, as well as the following values.

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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The specified interface is not supported.

</td>
</tr>
</table>
 




## -remarks



The COM library in the process where unmarshaling is to occur calls the proxy's implementation of this method.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
You do not call this method directly. There are, however, some situations in which you might call it indirectly through a call to <a href="https://msdn.microsoft.com/d0eac0da-2f41-40c4-b756-31bc22752c17">CoUnmarshalInterface</a>. For example, if you are implementing a stub, your implementation would call <b>CoUnmarshalInterface</b> when the stub receives an interface pointer as a parameter in a method call.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The proxy's implementation should read the data written to the stream by the original object's implementation of <a href="https://msdn.microsoft.com/c48a7123-bd00-4ff3-8880-7fc4b99e4299">IMarshal::MarshalInterface</a> and use that data to initialize the proxy object whose CLSID was returned by the marshaling stub's call to the original object's implementation of <a href="https://msdn.microsoft.com/900a0f19-dcd5-4135-bab8-c191ec7e95e4">IMarshal::GetUnmarshalClass</a>.

To return the appropriate interface pointer, the proxy implementation can simply call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on itself, passing the <i>riid</i> and <i>ppv</i> parameters. However, your implementation of <b>UnmarshalInterface</b> is free to create a different object and, if necessary, return a pointer to it.

Just before exiting, even if exiting with an error, your implementation should reposition the seek pointer in the stream immediately after the last byte of data read.




## -see-also




<a href="https://msdn.microsoft.com/d0eac0da-2f41-40c4-b756-31bc22752c17">CoUnmarshalInterface</a>



<a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a>
 

 

