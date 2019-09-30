---
UID: NF:mfmediaengine.IMFMediaKeySession.Update
title: IMFMediaKeySession::Update (mfmediaengine.h)
author: windows-sdk-content
description: Passes in a key value with any associated data required by the Content Decryption Module for the given key system.
old-location: mf\imfmediakeysession_update.htm
tech.root: medfound
ms.assetid: 29e66037-5f18-4724-b6f2-d85555e6af69
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFMediaKeySession interface [Media Foundation],Update method, IMFMediaKeySession.Update, IMFMediaKeySession::Update, Update, Update method [Media Foundation], Update method [Media Foundation],IMFMediaKeySession interface, mf.imfmediakeysession_update, mfmediaengine/IMFMediaKeySession::Update
ms.topic: method
f1_keywords: 
 - "mfmediaengine/IMFMediaKeySession.Update"
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - mfmediaengine.h
api_name:
 - IMFMediaKeySession.Update
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaKeySession::Update


## -description


Passes in a key value with any associated data required by the Content Decryption Module for the given key system.


## -parameters




### -param key


### -param cb

The count in bytes of <i>key</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession">IMFMediaKeySession</a>
 

 

