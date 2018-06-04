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

# RoGetBufferMarshaler function


## -description


Provides a standard IBuffer marshaler to implement the semantics associated with the IBuffer interface when it is marshaled.


## -parameters




### -param bufferMarshaler [out]

pointer to Windows Runtime IBuffer marshaler


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Provided for Windows Runtime language projections.

Custom IBuffer implementations are expected to be marshaled so that the remote instance eventually copies its contents back to the original instance. The <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a> implementation provided by this method handles the copy by marshaling the current value of the IBuffer and specifying a platform-provided unmarshal COM class that creates an instance with identical IBuffer contents, length, and capacity.  

The <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a> implementation clones its contents to the original instance when the caller sets the Length property.




## -see-also




<a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a>
 

 

