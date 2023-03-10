---
UID: NF:audioengineendpoint.IAudioDeviceEndpoint.WriteExclusiveModeParametersToSharedMemory
title: IAudioDeviceEndpoint::WriteExclusiveModeParametersToSharedMemory (audioengineendpoint.h)
description: Creates and writes the exclusive-mode parameters to shared memory.
helpviewer_keywords: ["IAudioDeviceEndpoint interface [Remote Desktop Services]","WriteExclusiveModeParametersToSharedMemory method","IAudioDeviceEndpoint.WriteExclusiveModeParametersToSharedMemory","IAudioDeviceEndpoint::WriteExclusiveModeParametersToSharedMemory","WriteExclusiveModeParametersToSharedMemory","WriteExclusiveModeParametersToSharedMemory method [Remote Desktop Services]","WriteExclusiveModeParametersToSharedMemory method [Remote Desktop Services]","IAudioDeviceEndpoint interface","audioengineendpoint/IAudioDeviceEndpoint::WriteExclusiveModeParametersToSharedMemory","termserv.iaudiodeviceendpoint_writeexclusivemodeparameterstosharedmemory"]
old-location: termserv\iaudiodeviceendpoint_writeexclusivemodeparameterstosharedmemory.htm
tech.root: TermServ
ms.assetid: 0484432a-4bbe-4892-8888-f11d6384d387
ms.date: 12/05/2018
ms.keywords: IAudioDeviceEndpoint interface [Remote Desktop Services],WriteExclusiveModeParametersToSharedMemory method, IAudioDeviceEndpoint.WriteExclusiveModeParametersToSharedMemory, IAudioDeviceEndpoint::WriteExclusiveModeParametersToSharedMemory, WriteExclusiveModeParametersToSharedMemory, WriteExclusiveModeParametersToSharedMemory method [Remote Desktop Services], WriteExclusiveModeParametersToSharedMemory method [Remote Desktop Services],IAudioDeviceEndpoint interface, audioengineendpoint/IAudioDeviceEndpoint::WriteExclusiveModeParametersToSharedMemory, termserv.iaudiodeviceendpoint_writeexclusivemodeparameterstosharedmemory
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioDeviceEndpoint::WriteExclusiveModeParametersToSharedMemory
 - audioengineendpoint/IAudioDeviceEndpoint::WriteExclusiveModeParametersToSharedMemory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AudioEngineEndpoint.h
api_name:
 - IAudioDeviceEndpoint.WriteExclusiveModeParametersToSharedMemory
---

# IAudioDeviceEndpoint::WriteExclusiveModeParametersToSharedMemory


## -description

The 
   <b>WriteExclusiveModeParametersToSharedMemory</b> 
   method creates and writes the exclusive-mode parameters to shared memory.

## -parameters

### -param hTargetProcess [in]

The handle of the process for which the handles
    will be duplicated.

### -param hnsPeriod [in]

The periodicity, in 100-nanosecond units, of the device. This value must fall within the range of the 
      minimum and maximum periodicity of the device represented by the endpoint.

### -param hnsBufferDuration [in]

The buffer duration, in 100-nanosecond units, requested by the client.

### -param u32LatencyCoefficient [in]

The latency coefficient of the audio endpoint. A client can obtain the actual latency of the endpoint by 
      calling the <a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpoint-getlatency">IAudioEndpoint::GetLatency</a> 
      method.

### -param pu32SharedMemorySize [out]

Receives the size of the memory area shared by the service and the process.

### -param phSharedMemory [out]

Receives a handle to the memory area shared by the service and the process.

## -returns

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

This method is used to provide handles and parameters of the audio service of the endpoint to the client 
    process for use in exclusive mode. This method fails if the endpoint object is fully initialized through the 
    <a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudiodeviceendpoint-setbuffer">IAudioDeviceEndpoint::SetBuffer</a> 
    method call.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client 
    applications.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint">IAudioDeviceEndpoint</a>