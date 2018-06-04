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

# CoGetInterfaceAndReleaseStream function


## -description


Unmarshals a buffer containing an interface pointer and releases the stream when an interface pointer has been marshaled from another thread to the calling thread.


## -parameters




### -param pStm [in]

A pointer to the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface on the stream to be unmarshaled.


### -param iid [in]

A reference to the identifier of the interface requested from the unmarshaled object.


### -param ppv [out]

The address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppv</i> contains the requested interface pointer to the unmarshaled interface.


## -returns



This function can return the standard return values S_OK and E_INVALIDARG, as well as any of the values returned by <a href="https://msdn.microsoft.com/d0eac0da-2f41-40c4-b756-31bc22752c17">CoUnmarshalInterface</a>.




## -remarks



<div class="alert"><b>Important</b>  <p class="note">Security Note: Calling this method with untrusted data is a security risk. Call this method only with trusted data. For more information, see <a href="http://go.microsoft.com/fwlink/?LinkId=798821">Untrusted Data Security Risks</a>.

</div>
<div> </div>
The <b>CoGetInterfaceAndReleaseStream</b> function performs the following tasks: 

<ul>
<li>Calls <a href="https://msdn.microsoft.com/d0eac0da-2f41-40c4-b756-31bc22752c17">CoUnmarshalInterface</a> to unmarshal an interface pointer previously passed in a call to <a href="https://msdn.microsoft.com/c9ab8713-8604-4f0b-a11b-bdfb7d595d95">CoMarshalInterThreadInterfaceInStream</a>.
</li>
<li>Releases the stream pointer. Even if the unmarshaling fails, the stream is still released because there is no effective way to recover from a failure of this kind.
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/c9ab8713-8604-4f0b-a11b-bdfb7d595d95">CoMarshalInterThreadInterfaceInStream</a>



<a href="https://msdn.microsoft.com/d0eac0da-2f41-40c4-b756-31bc22752c17">CoUnmarshalInterface</a>
 

 

