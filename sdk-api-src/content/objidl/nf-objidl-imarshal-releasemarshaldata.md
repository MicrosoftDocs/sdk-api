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

# IMarshal::ReleaseMarshalData


## -description


Destroys a marshaled data packet.


## -parameters




### -param pStm [in]

A pointer to a stream that contains the data packet to be destroyed.


## -returns



This method can return the standard return values S_OK and E_FAIL, as well as any of the stream-access errors for the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface.




## -remarks



If an object's marshaled data packet does not get unmarshaled in the client process space and the packet is no longer needed, the client calls <b>ReleaseMarshalData</b> on the proxy's <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a> implementation to instruct the object to destroy the data packet. The call occurs within the <a href="https://msdn.microsoft.com/a642a20f-3a3c-46bc-b833-e424dab3a16d">CoReleaseMarshalData</a> function. The data packet serves as an additional reference on the object, and releasing the data is like releasing an interface pointer by calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>.

If the marshaled data packet somehow does not arrive in the client process or if <b>ReleaseMarshalData</b> is not successfully re-created in the proxy, COM can call this method on the object itself.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
You will rarely if ever have occasion to call this method yourself. A possible exception would be if you were to implement <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a> on a class factory for a class object on which you are also implementing <b>IMarshal</b>. In this case, if you were marshaling the object to a table where it could be retrieved by multiple clients, you might, as part of your unmarshaling routine, call <b>ReleaseMarshalData</b> to release the data packet for each proxy.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If your implementation stores state information about marshaled data packets, you can use this method to release the state information associated with the data packet represented by <i>pStm</i>. Your implementation should also position the seek pointer in the stream past the last byte of data.




## -see-also




<a href="https://msdn.microsoft.com/a642a20f-3a3c-46bc-b833-e424dab3a16d">CoReleaseMarshalData</a>



<a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a>
 

 

