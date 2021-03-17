---
UID: NF:devicetopology.IDeviceTopology.GetPartById
title: IDeviceTopology::GetPartById (devicetopology.h)
description: The GetPartById method gets a part that is identified by its local ID.
helpviewer_keywords: ["GetPartById","GetPartById method [Core Audio]","GetPartById method [Core Audio]","IDeviceTopology interface","IDeviceTopology interface [Core Audio]","GetPartById method","IDeviceTopology.GetPartById","IDeviceTopology::GetPartById","IDeviceTopologyGetPartById","coreaudio.idevicetopology_getpartbyid","devicetopology/IDeviceTopology::GetPartById"]
old-location: coreaudio\idevicetopology_getpartbyid.htm
tech.root: CoreAudio
ms.assetid: 03310040-2081-47cf-88aa-6281c6bea56e
ms.date: 12/05/2018
ms.keywords: GetPartById, GetPartById method [Core Audio], GetPartById method [Core Audio],IDeviceTopology interface, IDeviceTopology interface [Core Audio],GetPartById method, IDeviceTopology.GetPartById, IDeviceTopology::GetPartById, IDeviceTopologyGetPartById, coreaudio.idevicetopology_getpartbyid, devicetopology/IDeviceTopology::GetPartById
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
 - IDeviceTopology::GetPartById
 - devicetopology/IDeviceTopology::GetPartById
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
 - IDeviceTopology.GetPartById
---

# IDeviceTopology::GetPartById


## -description

The <b>GetPartById</b> method gets a part that is identified by its local ID.

## -parameters

### -param nId [in]

The part to get. This parameter is the local ID of the part. For more information, see Remarks.

### -param ppPart [out]

Pointer to a pointer variable into which the method writes the address of the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart</a> interface of the part object that is identified by <i>nId</i>. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>GetPartById</b> call fails,  <i>*ppPart</i> is <b>NULL</b>.

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
Parameter <i>nId</i> is not a valid local ID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>ppPart</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

A local ID is a number that uniquely identifies a part among all the parts in a device topology. The <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudioinputselector-getselection">IAudioInputSelector::GetSelection</a> and <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudiooutputselector-getselection">IAudioOutputSelector::GetSelection</a> methods retrieve the local ID of a connected part. The <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudioinputselector-setselection">IAudioInputSelector::SetSelection</a> and <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudiooutputselector-setselection">IAudioOutputSelector::SetSelection</a> methods select the input or output that is connected to a part that is identified by its local ID. When you have a pointer to a part object, you can call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getlocalid">IPart::GetLocalId</a> method to get the local ID of the part.

## -see-also

<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudioinputselector-getselection">IAudioInputSelector::GetSelection</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudioinputselector-setselection">IAudioInputSelector::SetSelection</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudiooutputselector-getselection">IAudioOutputSelector::GetSelection</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudiooutputselector-setselection">IAudioOutputSelector::SetSelection</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-idevicetopology">IDeviceTopology Interface</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getlocalid">IPart::GetLocalId</a>