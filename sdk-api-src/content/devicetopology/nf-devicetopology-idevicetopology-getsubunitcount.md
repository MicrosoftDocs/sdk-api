---
UID: NF:devicetopology.IDeviceTopology.GetSubunitCount
title: IDeviceTopology::GetSubunitCount (devicetopology.h)
description: The GetSubunitCount method gets the number of subunits in the device topology.
helpviewer_keywords: ["GetSubunitCount","GetSubunitCount method [Core Audio]","GetSubunitCount method [Core Audio]","IDeviceTopology interface","IDeviceTopology interface [Core Audio]","GetSubunitCount method","IDeviceTopology.GetSubunitCount","IDeviceTopology::GetSubunitCount","IDeviceTopologyGetSubunitCount","coreaudio.idevicetopology_getsubunitcount","devicetopology/IDeviceTopology::GetSubunitCount"]
old-location: coreaudio\idevicetopology_getsubunitcount.htm
tech.root: CoreAudio
ms.assetid: 70fa57bb-56fe-4f8c-9967-10714f1cba22
ms.date: 12/05/2018
ms.keywords: GetSubunitCount, GetSubunitCount method [Core Audio], GetSubunitCount method [Core Audio],IDeviceTopology interface, IDeviceTopology interface [Core Audio],GetSubunitCount method, IDeviceTopology.GetSubunitCount, IDeviceTopology::GetSubunitCount, IDeviceTopologyGetSubunitCount, coreaudio.idevicetopology_getsubunitcount, devicetopology/IDeviceTopology::GetSubunitCount
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
 - IDeviceTopology::GetSubunitCount
 - devicetopology/IDeviceTopology::GetSubunitCount
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
 - IDeviceTopology.GetSubunitCount
---

# IDeviceTopology::GetSubunitCount


## -description

The <b>GetSubunitCount</b> method gets the number of subunits in the device topology.

## -parameters

### -param pCount [out]

Pointer to a <b>UINT</b> variable into which the method writes the subunit count (the number of subunits in the device topology).

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
Pointer <i>pCount</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-idevicetopology">IDeviceTopology Interface</a>