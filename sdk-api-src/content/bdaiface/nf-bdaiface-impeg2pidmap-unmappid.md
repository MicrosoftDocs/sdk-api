---
UID: NF:bdaiface.IMPEG2PIDMap.UnmapPID
title: IMPEG2PIDMap::UnmapPID
author: windows-sdk-content
description: The UnmapPID method unmaps one or more PIDs.
old-location: dshow\impeg2pidmap_unmappid.htm
tech.root: DirectShow
ms.assetid: 1ad866c7-672e-4f96-a384-bbf78a78b8f5
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IMPEG2PIDMap interface [DirectShow],UnmapPID method, IMPEG2PIDMap.UnmapPID, IMPEG2PIDMap::UnmapPID, IMPEG2PIDMapUnmapPID, UnmapPID, UnmapPID method [DirectShow], UnmapPID method [DirectShow],IMPEG2PIDMap interface, bdaiface/IMPEG2PIDMap::UnmapPID, dshow.impeg2pidmap_unmappid
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMPEG2PIDMap.UnmapPID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMPEG2PIDMap::UnmapPID


## -description



The <code>UnmapPID</code> method unmaps one or more PIDs.




## -parameters




### -param culPID [in]

The number of elements in the <i>pulPID</i> array.


### -param pulPID [in]

Pointer to an array of size <i>culPID</i>, allocated by the caller. Each element in the array contains a PID to be unmapped


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



On output pins for audio and video streams, there will typically be only one PID mapped at any given time. On an output pin such as one delivering the PSI stream to the Transport Information Filter, there may be multiple PIDs mapped to a single pin. Use the <a href="https://msdn.microsoft.com/en-us/library/Dd376605(v=VS.85).aspx">IEnumPIDMap</a> methods to determine which PIDs are mapped to the pin, and then fill in the <i>pulPID</i> array with those values.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd407132(v=VS.85).aspx">IMPEG2PIDMap Interface</a>
 

 

