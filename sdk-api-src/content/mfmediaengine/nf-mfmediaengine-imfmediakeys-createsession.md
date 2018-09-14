---
UID: NF:mfmediaengine.IMFMediaKeys.CreateSession
title: IMFMediaKeys::CreateSession
author: windows-sdk-content
description: Creates a media key session object using the specified initialization data and custom data. .
old-location: mf\imfmediakeys_createsession.htm
tech.root: medfound
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: CreateSession, CreateSession method [Media Foundation], CreateSession method [Media Foundation],IMFMediaKeys interface, IMFMediaKeys interface [Media Foundation],CreateSession method, IMFMediaKeys.CreateSession, IMFMediaKeys::CreateSession, mf.imfmediakeys_createsession, mfmediaengine/IMFMediaKeys::CreateSession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMFMediaKeys.CreateSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaKeys::CreateSession


## -description


Creates a media key session object using the specified initialization data and custom data.
.



## -parameters




### -param mimeType

The MIME type of the media container used for the content.


### -param initData

The initialization data for the key system. 


### -param cb

The count in bytes of <i>initData</i>.


### -param customData

Custom data sent to the key system.


### -param cbCustomData

The count in bytes of <i>cbCustomData</i>.


### -param notify

notify


### -param ppSession

The media key session.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0689d938-e0be-46d7-bfed-add431331a90">IMFMediaKeys</a>
 

 

