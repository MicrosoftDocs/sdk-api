---
UID: NF:audioengineendpoint.IAudioEndpoint.GetFrameFormat
title: IAudioEndpoint::GetFrameFormat
author: windows-sdk-content
description: Retrieves the format of the audio endpoint.
old-location: termserv\iaudioendpoint_getframeformat.htm
old-project: TermServ
ms.assetid: fb34ef19-4155-461e-a8d7-0a903e9d7c72
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetFrameFormat, GetFrameFormat method [Remote Desktop Services], GetFrameFormat method [Remote Desktop Services],IAudioEndpoint interface, IAudioEndpoint interface [Remote Desktop Services],GetFrameFormat method, IAudioEndpoint.GetFrameFormat, IAudioEndpoint::GetFrameFormat, audioengineendpoint/IAudioEndpoint::GetFrameFormat, termserv.iaudioendpoint_getframeformat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: AE_POSITION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioEndpoint.GetFrameFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioEndpoint::GetFrameFormat


## -description



        The <b>GetFrameFormat</b> method retrieves the format of the audio endpoint.


## -parameters




### -param ppFormat [out]

Receives a pointer to a <b>WAVEFORMATEX</b> structure that contains the  format information for the device that the audio endpoint represents. The implementation must allocate memory for the structure by using <b>CoTaskMemAlloc</b>. The caller must free the buffer by using <b>CoTaskMemFree</b>. For information about <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>, see the Windows SDK documentation.


## -returns



If the method succeeds, it returns <b>S_OK</b>.




## -remarks



This method must not be called from a real-time processing thread.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.




## -see-also




<a href="https://msdn.microsoft.com/a1bb3fe4-6051-4b9c-8270-70375e700f01">IAudioEndpoint</a>
 

 

