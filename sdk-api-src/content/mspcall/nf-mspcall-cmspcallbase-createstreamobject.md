---
UID: NF:mspcall.CMSPCallBase.CreateStreamObject
title: CMSPCallBase::CreateStreamObject
author: windows-sdk-content
description: The CreateStreamObject method is called by InternalCreateStream.
old-location: tapi3\cmspcallbase_createstreamobject.htm
tech.root: Tapi
ms.assetid: ac98dd08-4250-40f6-91a8-e1f67b94b51f
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CMSPCallBase interface [TAPI 2.2],CreateStreamObject method, CMSPCallBase.CreateStreamObject, CMSPCallBase::CreateStreamObject, CreateStreamObject, CreateStreamObject method [TAPI 2.2], CreateStreamObject method [TAPI 2.2],CMSPCallBase interface, _tapi3_cmspcallbase_createstreamobject, mspcall/CMSPCallBase::CreateStreamObject, tapi3.cmspcallbase_createstreamobject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mspcall.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspcall.h
api_name:
 - CMSPCallBase.CreateStreamObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMSPCallBase::CreateStreamObject


## -description


The 
<b>CreateStreamObject</b> method is called by 
<a href="https://msdn.microsoft.com/6f9cef2e-36dd-4095-9060-b6d37ccbc6d7">InternalCreateStream</a>. The derived class should <b>CreateInstance</b> on its stream object, do an ATL <b>_InternalQueryInterface</b> to obtain an 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> pointer from the stream object, and call the stream object's 
<a href="https://msdn.microsoft.com/bda49b8e-4ae5-4cf9-ae61-44fbf41e2cda">Init</a> method (on the stream object pointer, not the 
<b>ITStream</b> pointer).


## -parameters




### -param dwMediaType


<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">Media type</a> of stream to be created.


### -param Direction


<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">Direction</a> of stream.


### -param pGraph

Pointer to DirectShow <b>IMediaEvent</b> interface.


### -param ppStream

Pointer to 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interface.


## -see-also




<a href="https://msdn.microsoft.com/77b53b66-38fa-4823-9051-e857da8a7dd7">CMSPCallBase</a>
 

 

