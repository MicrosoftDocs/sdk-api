---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CoMarshalInterThreadInterfaceInStream function


## -description


Marshals an interface pointer from one thread to another thread in the same process.




## -parameters




### -param riid [in]

A reference to the identifier of the interface to be marshaled.


### -param pUnk [in]

A pointer to the interface to be marshaled, which must be derived from <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>. This parameter can be <b>NULL</b>.


### -param ppStm [out]

The address of the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>* pointer variable that receives the interface pointer to the stream that contains the marshaled interface.


## -returns



This function can return the standard return values E_OUTOFMEMORY and S_OK.




## -remarks



The <b>CoMarshalInterThreadInterfaceInStream</b> function enables an object to easily and reliably marshal an interface pointer to another thread in the same process. The stream returned in the <i>ppStm</i> parameter is guaranteed to behave correctly when a client running in the receiving thread attempts to unmarshal the pointer. The client can then call the <a href="https://msdn.microsoft.com/b529f65f-3208-4594-a772-d1cad3727dc1">CoGetInterfaceAndReleaseStream</a> to unmarshal the interface pointer and release the stream object.

The <b>CoMarshalInterThreadInterfaceInStream</b> function performs the following tasks:

<ol>
<li>
Creates a stream object.

</li>
<li>
Passes the stream object's IStream pointer to <a href="https://msdn.microsoft.com/04ca1217-eac1-43e2-b736-8d7522ce8592">CoMarshalInterface</a>.

</li>
<li>
Returns the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> pointer to the caller.

</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/b529f65f-3208-4594-a772-d1cad3727dc1">CoGetInterfaceAndReleaseStream</a>
 

 

