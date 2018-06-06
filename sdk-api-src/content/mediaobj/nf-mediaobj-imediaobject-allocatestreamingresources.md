---
UID: NF:mediaobj.IMediaObject.AllocateStreamingResources
title: IMediaObject::AllocateStreamingResources
author: windows-sdk-content
description: The AllocateStreamingResources method allocates any resources needed by the DMO. Calling this method is always optional.
old-location: dshow\imediaobject_allocatestreamingresources.htm
old-project: DirectShow
ms.assetid: cd608bf2-50a5-4037-aeb5-c5c380c3d6df
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: AllocateStreamingResources, AllocateStreamingResources method [DirectShow], AllocateStreamingResources method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],AllocateStreamingResources method, IMediaObject.AllocateStreamingResources, IMediaObject::AllocateStreamingResources, IMediaObjectAllocateStreamingResources, dshow.imediaobject_allocatestreamingresources, mediaobj/IMediaObject::AllocateStreamingResources
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
<li>If the application never calls this method, the DMO allocates resources within a call to <a href="https://msdn.microsoft.com/f52e9586-f65d-418f-8c1a-c97c0a81d253">IMediaObject::ProcessInput</a> or <a href="https://msdn.microsoft.com/1a3b1192-f1e9-4f04-b543-d38692502b8e">IMediaObject::ProcessOutput</a>.</li>
</ul>
If the DMO supports this method, it should also support the <a href="https://msdn.microsoft.com/c4d2dbf1-45c9-47a2-a21f-5eb04f828ec1">IMediaObject::FreeStreamingResources</a> method.




## -see-also




<a href="https://msdn.microsoft.com/a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b">IMediaObject Interface</a>
 

 

