---
UID: NN:audioengineendpoint.IAudioEndpointRT
title: IAudioEndpointRT (audioengineendpoint.h)
description: Gets the difference between the current read and write positions in the endpoint buffer.
helpviewer_keywords: ["IAudioEndpointRT","IAudioEndpointRT interface [Remote Desktop Services]","IAudioEndpointRT interface [Remote Desktop Services]","described","audioengineendpoint/IAudioEndpointRT","termserv.iaudioendpointrt"]
old-location: termserv\iaudioendpointrt.htm
tech.root: TermServ
ms.assetid: 3fb05ce4-a3be-4c84-8e03-71213f453f74
ms.date: 12/05/2018
ms.keywords: IAudioEndpointRT, IAudioEndpointRT interface [Remote Desktop Services], IAudioEndpointRT interface [Remote Desktop Services],described, audioengineendpoint/IAudioEndpointRT, termserv.iaudioendpointrt
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
 - IAudioEndpointRT
 - audioengineendpoint/IAudioEndpointRT
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
 - IAudioEndpointRT
---

# IAudioEndpointRT interface


## -description

Gets the difference between the current read and write positions in the endpoint buffer. The 
    <b>IAudioEndpointRT</b> interface is used by the audio 
    engine.

<b>IAudioEndpointRT</b> methods can be called from a 
    real-time processing thread. The implementation of the methods of this interface must not block, access paged 
    memory, or call any blocking system routines.

## -inheritance

The <b>IAudioEndpointRT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioEndpointRT</b> also has these types of members:

## -remarks

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client 
    applications.
