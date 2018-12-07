---
UID: NF:mediaobj.IMediaObjectInPlace.Clone
title: IMediaObjectInPlace::Clone
author: windows-sdk-content
description: The Clone method creates a copy of the DMO in its current state.
old-location: dshow\imediaobjectinplace_clone.htm
tech.root: DirectShow
ms.assetid: 6660afa8-3502-4e88-925b-192e06346243
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Clone, Clone method [DirectShow], Clone method [DirectShow],IMediaObjectInPlace interface, IMediaObjectInPlace interface [DirectShow],Clone method, IMediaObjectInPlace.Clone, IMediaObjectInPlace::Clone, IMediaObjectInPlaceClone, dshow.imediaobjectinplace_clone, mediaobj/IMediaObjectInPlace::Clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mediaobj.h
req.include-header: Dmo.h
req.target-type: Windows
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObjectInPlace.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaObjectInPlace::Clone


## -description



The <code>Clone</code> method creates a copy of the DMO in its current state.




## -parameters




### -param ppMediaObject [out]

Address of a pointer to receive the new DMO's <a href="https://msdn.microsoft.com/c2105141-6c5e-4edb-aa3b-3227ca223329">IMediaObjectInPlace</a> interface.


## -returns



Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



If the method succeeds, the <b>IMediaObjectInPlace</b> interface that it returns has an outstanding reference count. Be sure to release the interface when you are finished using it.




## -see-also




<a href="https://msdn.microsoft.com/c2105141-6c5e-4edb-aa3b-3227ca223329">IMediaObjectInPlace Interface</a>
 

 

