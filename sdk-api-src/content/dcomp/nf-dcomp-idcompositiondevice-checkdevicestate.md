---
UID: NF:dcomp.IDCompositionDevice.CheckDeviceState
title: IDCompositionDevice::CheckDeviceState
author: windows-sdk-content
description: Determines whether the DirectComposition device object is still valid.
old-location: directcomp\idcompositiondevice_checkdevicestate.htm
tech.root: directcomp
ms.assetid: F9916B1E-8713-4758-963A-DFD0F916FF2C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CheckDeviceState, CheckDeviceState method [DirectComposition], CheckDeviceState method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CheckDeviceState method, IDCompositionDevice.CheckDeviceState, IDCompositionDevice::CheckDeviceState, dcomp/IDCompositionDevice::CheckDeviceState, directcomp.idcompositiondevice_checkdevicestate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDevice.CheckDeviceState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice::CheckDeviceState


## -description


Determines whether the DirectComposition device object is still valid.


## -parameters




### -param pfValid [out]

TRUE if the  DirectComposition device object is still valid; otherwise FALSE.


## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



	If the Microsoft DirectX Graphics Infrastructure (DXGI) device is lost, the DirectComposition device associated with the DXGI device is also lost. When it detects a lost device, DirectComposition sends the <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a>  message to all windows that are composing DirectComposition content using the lost device. An application should call <b>CheckDeviceState</b> in response to each  <b>WM_PAINT</b> message to ensure that the DirectComposition device object is still valid. The application must take steps to recover content if the device object becomes invalid. Steps include creating new DXGI and DirectComposition devices, and recreating all content. (It’s not possible to create just a new DXGI device and associate it with the existing DirectComposition device.)  The system ensures that the device object remains valid between <b>WM_PAINT</b> messages. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh437392(v=VS.85).aspx">IDCompositionDevice</a>
 

 

