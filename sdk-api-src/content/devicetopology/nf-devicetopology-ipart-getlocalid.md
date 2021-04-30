---
UID: NF:devicetopology.IPart.GetLocalId
title: IPart::GetLocalId (devicetopology.h)
description: The GetLocalId method gets the local ID of this part.
helpviewer_keywords: ["GetLocalId","GetLocalId method [Core Audio]","GetLocalId method [Core Audio]","IPart interface","IPart interface [Core Audio]","GetLocalId method","IPart.GetLocalId","IPart::GetLocalId","IPartGetLocalId","coreaudio.ipart_getlocalid","devicetopology/IPart::GetLocalId"]
old-location: coreaudio\ipart_getlocalid.htm
tech.root: CoreAudio
ms.assetid: d5ca4908-1822-485c-a04a-0eeee1e384a8
ms.date: 12/05/2018
ms.keywords: GetLocalId, GetLocalId method [Core Audio], GetLocalId method [Core Audio],IPart interface, IPart interface [Core Audio],GetLocalId method, IPart.GetLocalId, IPart::GetLocalId, IPartGetLocalId, coreaudio.ipart_getlocalid, devicetopology/IPart::GetLocalId
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
 - IPart::GetLocalId
 - devicetopology/IPart::GetLocalId
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
 - IPart.GetLocalId
---

# IPart::GetLocalId


## -description

The <b>GetLocalId</b> method gets the local ID of this part.

## -parameters

### -param pnId [out]

Pointer to a <b>UINT</b> variable into which the method writes the local ID of this part.

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
Pointer <i>pnId</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

When you have a pointer to a part object, you can call this method to get the local ID of the part. A local ID is a number that uniquely identifies a part among all parts in a device topology.

The <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudioinputselector-getselection">IAudioInputSelector::GetSelection</a> and <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudiooutputselector-getselection">IAudioOutputSelector::GetSelection</a> methods retrieve the local ID of a connected part. The <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudioinputselector-setselection">IAudioInputSelector::SetSelection</a> and <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudiooutputselector-setselection">IAudioOutputSelector::SetSelection</a> methods select the input or output that is connected to a part that is identified by its local ID. The <a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getpartbyid">IDeviceTopology::GetPartById</a> method gets a part that is identified by its local ID.

For code examples that use the <b>GetLocalId</b> method, see the following topics:

<ul>
<li>
<a href="/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/using-the-ikscontrol-interface-to-access-audio-properties">Using the IKsControl Interface to Access Audio Properties</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudioinputselector-getselection">IAudioInputSelector::GetSelection</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudioinputselector-setselection">IAudioInputSelector::SetSelection</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudiooutputselector-getselection">IAudioOutputSelector::GetSelection</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudiooutputselector-setselection">IAudioOutputSelector::SetSelection</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getpartbyid">IDeviceTopology::GetPartById</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>