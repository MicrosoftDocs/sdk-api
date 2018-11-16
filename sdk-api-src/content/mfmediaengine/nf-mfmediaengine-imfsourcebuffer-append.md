---
UID: NF:mfmediaengine.IMFSourceBuffer.Append
title: IMFSourceBuffer::Append
author: windows-sdk-content
description: Appends the specified media segment to the IMFSourceBuffer.
old-location: mf\imfsourcebuffer_append.htm
tech.root: medfound
ms.assetid: 824fa23d-57d9-411a-af8a-fb65dca124b2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Append, Append method [Media Foundation], Append method [Media Foundation],IMFSourceBuffer interface, IMFSourceBuffer interface [Media Foundation],Append method, IMFSourceBuffer.Append, IMFSourceBuffer::Append, mf.imfsourcebuffer_append, mfmediaengine/IMFSourceBuffer::Append
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
 - IMFSourceBuffer.Append
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfmediaengine.h
: 
- IMFSourceBuffer.Append
: 
---

# IMFSourceBuffer::Append


## -description


Appends the specified media segment to the <a href="https://msdn.microsoft.com/f241e232-9013-46d0-be97-2d6b5246cff3">IMFSourceBuffer</a>.


## -parameters




### -param pData [in]

The media data to append.


### -param len [in]

The length of the media data stored in <i>pData</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f241e232-9013-46d0-be97-2d6b5246cff3">IMFSourceBuffer</a>
 

 

