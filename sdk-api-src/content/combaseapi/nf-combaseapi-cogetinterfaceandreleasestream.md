---
UID: NF:combaseapi.CoGetInterfaceAndReleaseStream
title: CoGetInterfaceAndReleaseStream function
author: windows-sdk-content
description: Unmarshals a buffer containing an interface pointer and releases the stream when an interface pointer has been marshaled from another thread to the calling thread.
old-location: com\cogetinterfaceandreleasestream.htm
tech.root: com
ms.assetid: b529f65f-3208-4594-a772-d1cad3727dc1
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CoGetInterfaceAndReleaseStream, CoGetInterfaceAndReleaseStream function [COM], _com_CoGetInterfaceAndReleaseStream, com.cogetinterfaceandreleasestream, combaseapi/CoGetInterfaceAndReleaseStream
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
 - CoGetInterfaceAndReleaseStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CoGetInterfaceAndReleaseStream
: 
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
 

 

