---
UID: NF:devicetopology.IDeviceTopology.GetSignalPath
title: IDeviceTopology::GetSignalPath (devicetopology.h)
description: The GetSignalPath method gets a list of parts in the signal path that links two parts, if the path exists.
helpviewer_keywords: ["GetSignalPath","GetSignalPath method [Core Audio]","GetSignalPath method [Core Audio]","IDeviceTopology interface","IDeviceTopology interface [Core Audio]","GetSignalPath method","IDeviceTopology.GetSignalPath","IDeviceTopology::GetSignalPath","IDeviceTopologyGetSignalPath","coreaudio.idevicetopology_getsignalpath","devicetopology/IDeviceTopology::GetSignalPath"]
old-location: coreaudio\idevicetopology_getsignalpath.htm
tech.root: CoreAudio
ms.assetid: 3f32ba6a-a82c-4c2c-8433-ebedd8799615
ms.date: 12/05/2018
ms.keywords: GetSignalPath, GetSignalPath method [Core Audio], GetSignalPath method [Core Audio],IDeviceTopology interface, IDeviceTopology interface [Core Audio],GetSignalPath method, IDeviceTopology.GetSignalPath, IDeviceTopology::GetSignalPath, IDeviceTopologyGetSignalPath, coreaudio.idevicetopology_getsignalpath, devicetopology/IDeviceTopology::GetSignalPath
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
 - IDeviceTopology::GetSignalPath
 - devicetopology/IDeviceTopology::GetSignalPath
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
 - IDeviceTopology.GetSignalPath
---

# IDeviceTopology::GetSignalPath


## -description

The <b>GetSignalPath</b> method gets a list of parts in the signal path that links two parts, if the path exists.

## -parameters

### -param pIPartFrom [in]

Pointer to the "from" part. This parameter is a pointer to the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart</a> interface of the part at the beginning of the signal path.

### -param pIPartTo [in]

Pointer to the "to" part. This parameter is a pointer to the <b>IPart</b> interface of the part at the end of the signal path.

### -param bRejectMixedPaths [in]

Specifies whether to reject paths that contain mixed data. If <i>bRejectMixedPaths</i> is <b>TRUE</b> (nonzero), the method ignores any data path that contains a mixer (that is, a processing node that sums together two or more input signals). If <b>FALSE</b>, the method will try to find a path that connects the "from" and "to" parts regardless of whether the path contains a mixer.

### -param ppParts [out]

Pointer to a pointer variable into which the method writes the address of an <a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipartslist">IPartsList</a> interface instance. This interface encapsulates the list of parts in the signal path that connects the "from" part to the "to" part. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>GetSignalPath</b> call fails,  <i>*ppParts</i> is <b>NULL</b>.

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
Parameter <i>pIPartFrom</i>, <i>pIPartTo</i>, or <i>ppParts</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
No path linking the two parts was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pIPartFrom</i> or <i>pIPartTo</i> does not point to a valid <b>IPart</b> interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>

## -remarks

This method creates an <b>IPartsList</b> interface instance that contains a list of the parts that lie along the specified signal path. The parts in the parts list are ordered according to their relative positions in the signal path. The "to" part is the first item in the list and the "from" part is the last item in the list.

If the list contains <i>n</i> parts, the "to" and "from" parts are identified by list indexes 0 and <i>n</i>– 1, respectively. To get the number of parts in a parts list, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipartslist-getcount">IPartsList::GetCount</a> method. To retrieve a part by its index, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipartslist-getpart">IPartsList::GetPart</a> method.

The parts in the signal path must all be part of the same device topology. The path cannot span boundaries between device topologies.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-idevicetopology">IDeviceTopology Interface</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipartslist">IPartsList Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipartslist-getcount">IPartsList::GetCount</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipartslist-getpart">IPartsList::GetPart</a>