---
UID: NF:mmdeviceapi.IMMEndpoint.GetDataFlow
title: IMMEndpoint::GetDataFlow (mmdeviceapi.h)
description: The GetDataFlow method indicates whether the audio endpoint device is a rendering device or a capture device.
old-location: coreaudio\immendpoint_getdataflow.htm
tech.root: CoreAudio
ms.assetid: 01882c44-bf0c-4180-846e-c1e98c6fb472
ms.date: 12/05/2018
ms.keywords: GetDataFlow, GetDataFlow method [Core Audio], GetDataFlow method [Core Audio],IMMEndpoint interface, IMMEndpoint interface [Core Audio],GetDataFlow method, IMMEndpoint.GetDataFlow, IMMEndpoint::GetDataFlow, IMMEndpointGetDataFlow, coreaudio.immendpoint_getdataflow, mmdeviceapi/IMMEndpoint::GetDataFlow
f1_keywords:
- mmdeviceapi/IMMEndpoint.GetDataFlow
dev_langs:
- c++
req.header: mmdeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- Mmdeviceapi.h
api_name:
- IMMEndpoint.GetDataFlow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMMEndpoint::GetDataFlow


## -description



The <b>GetDataFlow</b> method indicates whether the audio endpoint device is a rendering device or a capture device.




## -parameters




### -param pDataFlow [out]

Pointer to a variable into which the method writes the data-flow direction of the endpoint device. The direction is indicated by one of the following <a href="https://docs.microsoft.com/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow">EDataFlow</a> enumeration constants:

eRender

eCapture

The data-flow direction for a rendering device is eRender. The data-flow direction for a capture device is eCapture.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>ppDataFlow</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint">IMMEndpoint Interface</a>
 

 

