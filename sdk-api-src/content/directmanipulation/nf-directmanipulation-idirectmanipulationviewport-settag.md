---
UID: NF:directmanipulation.IDirectManipulationViewport.SetTag
title: IDirectManipulationViewport::SetTag
author: windows-sdk-content
description: Sets a viewport tag.
old-location: directmanipulation\idirectmanipulationviewport_settag.htm
tech.root: directmanipulation
ms.assetid: f695845b-8980-45cd-8231-e3ce29ce322f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],SetTag method, IDirectManipulationViewport.SetTag, IDirectManipulationViewport::SetTag, SetTag, SetTag method [Direct Manipulation], SetTag method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_settag, directmanipulation/IDirectManipulationViewport::SetTag
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
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
 - DirectManipulation.h
api_name:
 - IDirectManipulationViewport.SetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationViewport::SetTag


## -description


Sets a viewport tag.


## -parameters




### -param object [in, optional]

The object portion of the tag.


### -param id [in]

The ID portion of the tag.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



A tag is a pairing of an integer ID with a Component Object Model (COM) object. It can be used by an app to identify the viewport.

The object parameter is optional, so that the method can set just an ID.



#### Examples

The following example shows the syntax for this method.


```
IUnknown* pUnk = ...;
UINT32 id = ...;

HRESULT hr = pRegion->SetTag(pUnk, id);

```





## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

