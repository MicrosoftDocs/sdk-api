---
UID: NF:mspcall.CMSPCallBase.CreateStreamObject
title: CMSPCallBase::CreateStreamObject
author: windows-sdk-content
description: The CreateStreamObject method is called by InternalCreateStream.
old-location: tapi3\cmspcallbase_createstreamobject.htm
old-project: Tapi
ms.assetid: ac98dd08-4250-40f6-91a8-e1f67b94b51f
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: CMSPCallBase interface [TAPI 2.2],CreateStreamObject method, CMSPCallBase.CreateStreamObject, CMSPCallBase::CreateStreamObject, CreateStreamObject, CreateStreamObject method [TAPI 2.2], CreateStreamObject method [TAPI 2.2],CMSPCallBase interface, _tapi3_cmspcallbase_createstreamobject, mspcall/CMSPCallBase::CreateStreamObject, tapi3.cmspcallbase_createstreamobject
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MSPEVENTITEM, *PMSPEVENTITEM
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
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CMSPCallBase::CreateStreamObject


## -description


The 
<b>CreateStreamObject</b> method is called by 
<a href="https://msdn.microsoft.com/6f9cef2e-36dd-4095-9060-b6d37ccbc6d7">InternalCreateStream</a>. The derived class should <b>CreateInstance</b> on its stream object, do an ATL <b>_InternalQueryInterface</b> to obtain an 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> pointer from the stream object, and call the stream object's 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541624">Init</a> method (on the stream object pointer, not the 
<b>ITStream</b> pointer).


## -parameters




### -param dwMediaType


<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">Media type</a> of stream to be created.


### -param Direction


<a href="https://msdn.microsoft.com/library/windows/hardware/ff547596">Direction</a> of stream.


### -param pGraph

Pointer to DirectShow <b>IMediaEvent</b> interface.


### -param ppStream

Pointer to 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interface.


## -see-also




<a href="https://msdn.microsoft.com/77b53b66-38fa-4823-9051-e857da8a7dd7">CMSPCallBase</a>
 

 

