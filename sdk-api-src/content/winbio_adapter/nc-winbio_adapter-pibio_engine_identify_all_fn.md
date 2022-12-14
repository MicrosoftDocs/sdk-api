---
UID: NC:winbio_adapter.PIBIO_ENGINE_IDENTIFY_ALL_FN
title: PIBIO_ENGINE_IDENTIFY_ALL_FN (winbio_adapter.h)
description: Determines the identities of any people who are currently in camera frame.
helpviewer_keywords: ["EngineAdapterIdentifyAll","EngineAdapterIdentifyAll callback function [Windows Biometric Framework API]","PIBIO_ENGINE_IDENTIFY_ALL_FN","PIBIO_ENGINE_IDENTIFY_ALL_FN callback","secbiomet.engineadapteridentifyall","winbio_adapter/EngineAdapterIdentifyAll"]
old-location: secbiomet\engineadapteridentifyall.htm
tech.root: SecBioMet
ms.assetid: B8B72654-D161-480B-AD3D-8ED236249562
ms.date: 12/05/2018
ms.keywords: EngineAdapterIdentifyAll, EngineAdapterIdentifyAll callback function [Windows Biometric Framework API], PIBIO_ENGINE_IDENTIFY_ALL_FN, PIBIO_ENGINE_IDENTIFY_ALL_FN callback, secbiomet.engineadapteridentifyall, winbio_adapter/EngineAdapterIdentifyAll
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PIBIO_ENGINE_IDENTIFY_ALL_FN
 - winbio_adapter/PIBIO_ENGINE_IDENTIFY_ALL_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - EngineAdapterIdentifyAll
---

# PIBIO_ENGINE_IDENTIFY_ALL_FN callback function


## -description

Called by the Windows Biometric Framework to determine the identities of any people who are currently in camera frame.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param PresenceCount [out]

Address of a variable that receives the number of presences detected by the function.

### -param PresenceArray [out]

Address of a variable that receives a pointer to an array of <a href="/windows/desktop/SecBioMet/winbio-presence">WINBIO_PRESENCE</a> elements.

## -returns

If the function succeeds, it returns <b>S_OK</b>. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_some_error </b></dt>
</dl>
</td>
<td width="60%">
Any error code will cause the Biometric Service to log the error and ignore the camera frame.

</td>
</tr>
</table>

## -remarks

The biometric service calls this method after it sends a new frame of data to the engine adapter.

After processing the data frame, this function should return one <a href="/windows/desktop/SecBioMet/winbio-presence">WINBIO_PRESENCE</a> element for each presence detected in the data frame.

In the event that the <b>EngineAdapterIdentifyAll</b> function can’t find any faces in frame, it returns an <b>HRESULT</b> of <b>S_OK</b> and sets the <i>PresenceCount</i> and <i>PresenceArray</i> return parameters to zero and <b>NULL</b>, respectively. In other words, a frame that doesn’t contain any human presences is not an error condition. 

The only time <b>EngineAdapterIdentifyAll</b> should return an <b>HRESULT</b> other than <b>S_OK</b> is if it doesn’t want the bio service to use the frame to update the Presence Monitor state. This should be a rare occurrence.
The engine adapter is responsible for allocating the array of <a href="/windows/desktop/SecBioMet/winbio-presence">WINBIO_PRESENCE</a> elements it returns in the <i>PresenceArray</i> parameter. It must allocate this memory from the process heap by using the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> function. After the array is created, it becomes the property of the Windows Biometric Framework. Because the Framework deallocates this memory after using it, your engine adapter must not attempt to deallocate the array or save a pointer to it. Failure to follow this rule will lead to heap corruption and possible crashes of the biometric service.


The values of the individual <a href="/windows/desktop/SecBioMet/winbio-presence">WINBIO_PRESENCE</a> items in the <i>PresenceArray</i> will determine the events generated for client applications. See the discussion of the <b>WINBIO_PRESENCE</b> structure for details.
