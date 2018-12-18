---
UID: NF:mediaobj.IMediaObject.AllocateStreamingResources
title: IMediaObject::AllocateStreamingResources
author: windows-sdk-content
description: The AllocateStreamingResources method allocates any resources needed by the DMO. Calling this method is always optional.
old-location: dshow\imediaobject_allocatestreamingresources.htm
tech.root: DirectShow
ms.assetid: cd608bf2-50a5-4037-aeb5-c5c380c3d6df
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AllocateStreamingResources, AllocateStreamingResources method [DirectShow], AllocateStreamingResources method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],AllocateStreamingResources method, IMediaObject.AllocateStreamingResources, IMediaObject::AllocateStreamingResources, IMediaObjectAllocateStreamingResources, dshow.imediaobject_allocatestreamingresources, mediaobj/IMediaObject::AllocateStreamingResources
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
 - IMediaObject.AllocateStreamingResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaObject::AllocateStreamingResources


## -description



The <code>AllocateStreamingResources</code> method allocates any resources needed by the DMO. Calling this method is always optional.




## -parameters






## -returns



Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



An application can call this method as a streaming optimization. It gives the DMO an opportunity to perform any time-consuming initializations before streaming begins. If you call this method, do so after you set the media types on the DMO, but before you make the first calls to <b>ProcessInput</b> or <b>ProcessOutput</b>.

This method is optional in the following sense:

<ul>
<li>If the DMO does not support this method, the method returns S_OK.</li>
<li>If the application never calls this method, the DMO allocates resources within a call to <a href="https://msdn.microsoft.com/en-us/library/Dd406959(v=VS.85).aspx">IMediaObject::ProcessInput</a> or <a href="https://msdn.microsoft.com/en-us/library/Dd406960(v=VS.85).aspx">IMediaObject::ProcessOutput</a>.</li>
</ul>
If the DMO supports this method, it should also support the <a href="https://msdn.microsoft.com/en-us/library/Dd406946(v=VS.85).aspx">IMediaObject::FreeStreamingResources</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd406926(v=VS.85).aspx">IMediaObject Interface</a>
 

 

