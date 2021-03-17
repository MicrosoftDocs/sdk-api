---
UID: NF:devicetopology.IDeviceTopology.GetSubunit
title: IDeviceTopology::GetSubunit (devicetopology.h)
description: The GetSubunit method gets the subunit that is specified by a subunit number.
helpviewer_keywords: ["GetSubunit","GetSubunit method [Core Audio]","GetSubunit method [Core Audio]","IDeviceTopology interface","IDeviceTopology interface [Core Audio]","GetSubunit method","IDeviceTopology.GetSubunit","IDeviceTopology::GetSubunit","IDeviceTopologyGetSubunit","coreaudio.idevicetopology_getsubunit","devicetopology/IDeviceTopology::GetSubunit"]
old-location: coreaudio\idevicetopology_getsubunit.htm
tech.root: CoreAudio
ms.assetid: 6251cabd-9284-4311-bd5c-0c5b6d9a9be4
ms.date: 12/05/2018
ms.keywords: GetSubunit, GetSubunit method [Core Audio], GetSubunit method [Core Audio],IDeviceTopology interface, IDeviceTopology interface [Core Audio],GetSubunit method, IDeviceTopology.GetSubunit, IDeviceTopology::GetSubunit, IDeviceTopologyGetSubunit, coreaudio.idevicetopology_getsubunit, devicetopology/IDeviceTopology::GetSubunit
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
 - IDeviceTopology::GetSubunit
 - devicetopology/IDeviceTopology::GetSubunit
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
 - IDeviceTopology.GetSubunit
---

# IDeviceTopology::GetSubunit


## -description

The <b>GetSubunit</b> method gets the subunit that is specified by a subunit number.

## -parameters

### -param nIndex [in]

The subunit number. If a device topology contains <i>n</i> subunits, the subunits are numbered from 0 to <i>n</i>– 1. To get the number of subunits in the device topology, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getsubunitcount">IDeviceTopology::GetSubunitCount</a> method.

### -param ppSubunit [out]

Pointer to a pointer variable into which the method writes the address of the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-isubunit">ISubunit</a> interface of the subunit object. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>GetSubunit</b> call fails,  <i>*ppSubunit</i> is <b>NULL</b>.

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
Pointer <i>ppSubunit</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-idevicetopology">IDeviceTopology Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getsubunitcount">IDeviceTopology::GetSubunitCount</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-isubunit">ISubunit Interface</a>