---
UID: NF:mspcall.CMSPCallBase.RemoveStream
title: CMSPCallBase::RemoveStream
author: windows-sdk-content
description: "(Interface RemoveStream) The RemoveStream method is called by the application to remove a stream from the call."
old-location: tapi3\cmspcallbase_removestream.htm
tech.root: TAPI
ms.assetid: 5e2b4261-ba0f-429a-aef5-974b2841bf0b
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CMSPCallBase interface [TAPI 2.2],RemoveStream method, CMSPCallBase.RemoveStream, CMSPCallBase::RemoveStream, RemoveStream, RemoveStream method [TAPI 2.2], RemoveStream method [TAPI 2.2],CMSPCallBase interface, _tapi3_cmspcallbase_removestream, mspcall/CMSPCallBase::RemoveStream, tapi3.cmspcallbase_removestream
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
 - CMSPCallBase.RemoveStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMSPCallBase::RemoveStream


## -description


(Interface 
<b>RemoveStream</b>) The 
<b>RemoveStream</b> method is called by the application to remove a stream from the call. Derived MSP call objects that do not want to allow applications to remove streams should override this to simply return TAPI_E_NOTSUPPORTED. (This is a good simplification strategy for many MSPs.) Derived call objects that do support removal of streams by the application should override this method to remove the stream object from the call object's list of streams and release the call's references to the stream. (Also  see the 
<a href="https://msdn.microsoft.com/86512d40-380b-4e98-840d-b7be99a86623">CMSPCallMultiGraph</a> implementation.)


## -parameters




### -param pStream

Pointer to 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interface to be removed.


## -see-also




<a href="https://msdn.microsoft.com/77b53b66-38fa-4823-9051-e857da8a7dd7">CMSPCallBase</a>
 

 

