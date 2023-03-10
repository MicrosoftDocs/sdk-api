---
UID: NF:devicetopology.IPart.GetTopologyObject
title: IPart::GetTopologyObject (devicetopology.h)
description: The GetTopologyObject method gets a reference to the IDeviceTopology interface of the device-topology object that contains this part.
helpviewer_keywords: ["GetTopologyObject","GetTopologyObject method [Core Audio]","GetTopologyObject method [Core Audio]","IPart interface","IPart interface [Core Audio]","GetTopologyObject method","IPart.GetTopologyObject","IPart::GetTopologyObject","IPartGetTopologyObject","coreaudio.ipart_gettopologyobject","devicetopology/IPart::GetTopologyObject"]
old-location: coreaudio\ipart_gettopologyobject.htm
tech.root: CoreAudio
ms.assetid: 5ad5fc66-6452-4d55-8c6a-a20a87431302
ms.date: 12/05/2018
ms.keywords: GetTopologyObject, GetTopologyObject method [Core Audio], GetTopologyObject method [Core Audio],IPart interface, IPart interface [Core Audio],GetTopologyObject method, IPart.GetTopologyObject, IPart::GetTopologyObject, IPartGetTopologyObject, coreaudio.ipart_gettopologyobject, devicetopology/IPart::GetTopologyObject
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
 - IPart::GetTopologyObject
 - devicetopology/IPart::GetTopologyObject
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
 - IPart.GetTopologyObject
---

# IPart::GetTopologyObject


## -description

The <b>GetTopologyObject</b> method gets a reference to the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-idevicetopology">IDeviceTopology</a> interface of the device-topology object that contains this part.

## -parameters

### -param ppTopology [out]

Pointer to a pointer variable into which the method writes the address of the <b>IDeviceTopology</b> interface of the device-topology object. The caller obtains a counted reference to the interface from this method. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>GetTopologyObject</b> call fails,  <i>*ppTopology</i> is <b>NULL</b>.

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
Pointer <i>ppTopology</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

For code examples that use this method, see the following topics:

<ul>
<li>
<a href="/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/using-the-ikscontrol-interface-to-access-audio-properties">Using the IKsControl Interface to Access Audio Properties</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-idevicetopology">IDeviceTopology Interface</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>