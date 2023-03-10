---
UID: NF:devicetopology.IDeviceTopology.GetConnector
title: IDeviceTopology::GetConnector (devicetopology.h)
description: The GetConnector method gets the connector that is specified by a connector number.
helpviewer_keywords: ["GetConnector","GetConnector method [Core Audio]","GetConnector method [Core Audio]","IDeviceTopology interface","IDeviceTopology interface [Core Audio]","GetConnector method","IDeviceTopology.GetConnector","IDeviceTopology::GetConnector","IDeviceTopologyGetConnector","coreaudio.idevicetopology_getconnector","devicetopology/IDeviceTopology::GetConnector"]
old-location: coreaudio\idevicetopology_getconnector.htm
tech.root: CoreAudio
ms.assetid: a2da5d1e-ecd3-411e-8428-f529569cc11d
ms.date: 12/05/2018
ms.keywords: GetConnector, GetConnector method [Core Audio], GetConnector method [Core Audio],IDeviceTopology interface, IDeviceTopology interface [Core Audio],GetConnector method, IDeviceTopology.GetConnector, IDeviceTopology::GetConnector, IDeviceTopologyGetConnector, coreaudio.idevicetopology_getconnector, devicetopology/IDeviceTopology::GetConnector
req.header: devicetopology.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDeviceTopology::GetConnector
 - devicetopology/IDeviceTopology::GetConnector
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IDeviceTopology.GetConnector
---

# IDeviceTopology::GetConnector


## -description

The <b>GetConnector</b> method gets the connector that is specified by a connector number.

## -parameters

### -param nIndex [in]

The connector number. If a device topology contains n connectors, the connectors are numbered 0 to n – 1. To get the number of connectors in the device topology, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getconnectorcount">IDeviceTopology::GetConnectorCount</a> method.

### -param ppConnector [out]

Pointer to a pointer variable into which the method writes the address of the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector</a> interface of the connector object. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>GetConnector</b> call fails,  <i>*ppConnector</i> is <b>NULL</b>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>nIndex</i> is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>ppConnector</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

For code examples that call the <b>GetConnector</b> method, see the implementations of the GetHardwareDeviceTopology and SelectCaptureDevice functions in <a href="/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector Interface</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-idevicetopology">IDeviceTopology Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getconnectorcount">IDeviceTopology::GetConnectorCount</a>