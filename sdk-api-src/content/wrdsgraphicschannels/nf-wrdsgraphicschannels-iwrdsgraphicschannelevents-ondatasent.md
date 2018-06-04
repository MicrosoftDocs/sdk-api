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

# IWRdsGraphicsChannelEvents::OnDataSent


## -description


Called when the <a href="https://msdn.microsoft.com/6ce627d8-078d-427a-b732-473d4f44f719">IWRdsGraphicsChannel::Write</a> method is called and the data has been sent. After this method has been called, the <i>pBuffer</i> parameter passed to the <a href="https://msdn.microsoft.com/6ce627d8-078d-427a-b732-473d4f44f719">IWRdsGraphicsChannel::Write</a> method is no longer needed and can be freed or reused.


## -parameters




### -param pWriteContext [in]

A user-defined interface pointer that is passed as the <i>pContext</i> parameter in the <a href="https://msdn.microsoft.com/6ce627d8-078d-427a-b732-473d4f44f719">IWRdsGraphicsChannel::Write</a> method.


### -param bCancelled




### -param pBuffer [in]

A pointer to a buffer that contains the data that was sent. The <i>cbBuffer</i> parameter contains the length of this buffer.


### -param cbBuffer [in]

The length, in bytes, of the data in <i>pBuffer</i>.


#### - bCanceled [in]

Contains <b>TRUE</b> if the connection was dropped during the write, or <b>FALSE</b> otherwise.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6ce627d8-078d-427a-b732-473d4f44f719">IWRdsGraphicsChannel::Write</a>



<a href="https://msdn.microsoft.com/59802a2d-bdb0-4792-b667-5095d4a02b06">IWRdsGraphicsChannelEvents</a>
 

 

