---
UID: NF:mfmediaengine.IMFSourceBuffer.Remove
title: IMFSourceBuffer::Remove
author: windows-sdk-content
description: Removes the media segments defined by the specified time range from the IMFSourceBuffer.
old-location: mf\imfsourcebuffer_remove.htm
tech.root: medfound
ms.assetid: 86536d73-18c0-4acc-81ec-72f1dfe400c5
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFSourceBuffer interface [Media Foundation],Remove method, IMFSourceBuffer.Remove, IMFSourceBuffer::Remove, Remove, Remove method [Media Foundation], Remove method [Media Foundation],IMFSourceBuffer interface, mf.imfsourcebuffer_remove, mfmediaengine/IMFSourceBuffer::Remove
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
 - IMFSourceBuffer.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSourceBuffer::Remove


## -description


Removes the media segments defined by the specified time range from the <a href="https://msdn.microsoft.com/f241e232-9013-46d0-be97-2d6b5246cff3">IMFSourceBuffer</a>.


## -parameters




### -param start [in]

The start of the time range.


### -param end [in]

The end of the time range.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f241e232-9013-46d0-be97-2d6b5246cff3">IMFSourceBuffer</a>
 

 

