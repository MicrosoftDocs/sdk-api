---
UID: NF:mediaobj.IMediaObject.FreeStreamingResources
title: IMediaObject::FreeStreamingResources
author: windows-sdk-content
description: The FreeStreamingResources method frees resources allocated by the DMO. Calling this method is always optional.
old-location: dshow\imediaobject_freestreamingresources.htm
old-project: DirectShow
ms.assetid: c4d2dbf1-45c9-47a2-a21f-5eb04f828ec1
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: FreeStreamingResources, FreeStreamingResources method [DirectShow], FreeStreamingResources method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],FreeStreamingResources method, IMediaObject.FreeStreamingResources, IMediaObject::FreeStreamingResources, IMediaObjectFreeStreamingResources, dshow.imediaobject_freestreamingresources, mediaobj/IMediaObject::FreeStreamingResources
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
 - IMediaObject.FreeStreamingResources
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMediaObject::FreeStreamingResources


## -description



The <code>FreeStreamingResources</code> method frees resources allocated by the DMO. Calling this method is always optional.




## -parameters






## -returns



Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



This method releases any resources that the <a href="https://msdn.microsoft.com/cd608bf2-50a5-4037-aeb5-c5c380c3d6df">IMediaObject::AllocateStreamingResources</a> method initializes.

If the DMO does not support this method, the method returns S_OK. If you call this method during streaming, the method fails and the DMO does not release any resources.

Regardless of whether the method fails or succeeds, the application can continue to call other methods on the DMO. The DMO might need to re-initialize resources that were previously freed.




## -see-also




<a href="https://msdn.microsoft.com/a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b">IMediaObject Interface</a>
 

 

