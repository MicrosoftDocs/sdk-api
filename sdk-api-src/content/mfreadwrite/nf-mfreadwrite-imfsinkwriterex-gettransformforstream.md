---
UID: NF:mfreadwrite.IMFSinkWriterEx.GetTransformForStream
title: IMFSinkWriterEx::GetTransformForStream
author: windows-sdk-content
description: Gets a pointer to a Media Foundation transform (MFT) for a specified stream.
old-location: mf\imfsinkwriterex_gettransformforstream.htm
tech.root: medfound
ms.assetid: 72EEC01F-ED62-4DD7-A18C-766D01705CAE
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetTransformForStream, GetTransformForStream method [Media Foundation], GetTransformForStream method [Media Foundation],IMFSinkWriterEx interface, IMFSinkWriterEx interface [Media Foundation],GetTransformForStream method, IMFSinkWriterEx.GetTransformForStream, IMFSinkWriterEx::GetTransformForStream, mf.imfsinkwriterex_gettransformforstream, mfreadwrite/IMFSinkWriterEx::GetTransformForStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - mfreadwrite.h
api_name:
 - IMFSinkWriterEx.GetTransformForStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSinkWriterEx::GetTransformForStream


## -description


Gets a pointer to a Media Foundation transform (MFT) for a specified stream.


## -parameters




### -param dwStreamIndex [in]

The zero-based index of a stream.


### -param dwTransformIndex [in]

The zero-based index of the MFT to retreive.


### -param pGuidCategory [out]

Receives a pointer to a GUID that specifies the category of the MFT. For a list of possible values, see <a href="https://msdn.microsoft.com/eca3ae3b-e40a-407d-986c-d0a85b891f52">MFT_CATEGORY</a>.


### -param ppTransform [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a> interface of the MFT. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/77E6CB22-E3B5-4D5E-8876-48582F75AA5C">IMFSinkWriterEx</a>
 

 

