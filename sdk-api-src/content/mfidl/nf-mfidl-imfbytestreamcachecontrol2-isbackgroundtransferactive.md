---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IMFByteStreamCacheControl2::IsBackgroundTransferActive


## -description


Queries whether background transfer is active.


## -parameters




### -param pfActive [out]

Receives the value <b>TRUE</b> if background transfer is currently active, or <b>FALSE</b> otherwise.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Background transfer might stop because the cache limit was reached (see <a href="https://msdn.microsoft.com/1DDC3D76-E28B-4B8C-B2CD-FE77E840D949">IMFByteStreamCacheControl2::SetCacheLimit</a>) or because the <a href="https://msdn.microsoft.com/9f0f7102-c839-4e92-a798-5ea31ceba013">IMFByteStreamCacheControl::StopBackgroundTransfer</a> method was called.




## -see-also




<a href="https://msdn.microsoft.com/A901F679-B6F2-4DB7-8EFC-EA61249B64FB">IMFByteStreamCacheControl2</a>
 

 

