---
UID: NF:bdaiface.IMPEG2PIDMap.MapPID
title: IMPEG2PIDMap::MapPID
author: windows-sdk-content
description: The MapPID method maps one or more PIDs to the pin.
old-location: dshow\impeg2pidmap_mappid.htm
old-project: DirectShow
ms.assetid: 22784e4a-2b02-4fc9-ba55-8c918ea38892
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IMPEG2PIDMap interface [DirectShow],MapPID method, IMPEG2PIDMap.MapPID, IMPEG2PIDMap::MapPID, IMPEG2PIDMapMapPID, MapPID, MapPID method [DirectShow], MapPID method [DirectShow],IMPEG2PIDMap interface, bdaiface/IMPEG2PIDMap::MapPID, dshow.impeg2pidmap_mappid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMPEG2PIDMap.MapPID
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IMPEG2PIDMap::MapPID


## -description



The <code>MapPID</code> method maps one or more PIDs to the pin.




## -parameters




### -param culPID [in]

The number of elements in the <i>pulPID</i> array.


### -param pulPID [in]

Pointer to an array of size <i>culPID</i>, allocated by the caller. Each element in the array contains a PID to be mapped.


### -param MediaSampleContent [in]

Variable of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff567719">MEDIA_SAMPLE_CONTENT</a> that specifies the contents of the stream.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



There may be no more than 255 distinct PIDs mapped at any given time. This includes the PIDs that the Demux maps internally for its own use; this number varies depending on the transport stream. This limitation should not present a problem in practice, because applications will typically map no more than a dozen PIDs on any given transport stream.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/45c09a02-7da8-460a-9a64-f012c2181b94">IMPEG2PIDMap Interface</a>
 

 

