---
UID: NN:audioengineendpoint.IAudioOutputEndpointRT
title: IAudioOutputEndpointRT (audioengineendpoint.h)
description: Gets the output buffer for each processing pass.
helpviewer_keywords: ["IAudioOutputEndpointRT","IAudioOutputEndpointRT interface [Remote Desktop Services]","IAudioOutputEndpointRT interface [Remote Desktop Services]","described","audioengineendpoint/IAudioOutputEndpointRT","termserv.iaudiooutputendpointrt"]
old-location: termserv\iaudiooutputendpointrt.htm
tech.root: TermServ
ms.assetid: b881b2f9-ffe9-46ff-94aa-eef0af172a3e
ms.date: 12/05/2018
ms.keywords: IAudioOutputEndpointRT, IAudioOutputEndpointRT interface [Remote Desktop Services], IAudioOutputEndpointRT interface [Remote Desktop Services],described, audioengineendpoint/IAudioOutputEndpointRT, termserv.iaudiooutputendpointrt
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioOutputEndpointRT
 - audioengineendpoint/IAudioOutputEndpointRT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioOutputEndpointRT
---

# IAudioOutputEndpointRT interface


## -description

Gets the output buffer for each processing pass. The  
    <b>IAudioOutputEndpointRT</b> interface is used by the 
    audio engine.

## -inheritance

The <b>IAudioOutputEndpointRT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioOutputEndpointRT</b> also has these types of members:

## -remarks

<b>IAudioOutputEndpointRT</b> methods can be called 
     from a real-time processing thread. The implementation of the methods of this interface must not block, access 
     paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client 
    applications.
