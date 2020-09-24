---
UID: NF:devicetopology.IPart.GetPartType
title: IPart::GetPartType (devicetopology.h)
description: The GetPartType method gets the part type of this part.
helpviewer_keywords: ["GetPartType","GetPartType method [Core Audio]","GetPartType method [Core Audio]","IPart interface","IPart interface [Core Audio]","GetPartType method","IPart.GetPartType","IPart::GetPartType","IPartGetPartType","coreaudio.ipart_getparttype","devicetopology/IPart::GetPartType"]
old-location: coreaudio\ipart_getparttype.htm
tech.root: CoreAudio
ms.assetid: 79af1dce-b946-4ef2-af36-4437603966da
ms.date: 12/05/2018
ms.keywords: GetPartType, GetPartType method [Core Audio], GetPartType method [Core Audio],IPart interface, IPart interface [Core Audio],GetPartType method, IPart.GetPartType, IPart::GetPartType, IPartGetPartType, coreaudio.ipart_getparttype, devicetopology/IPart::GetPartType
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
 - IPart::GetPartType
 - devicetopology/IPart::GetPartType
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
 - IPart.GetPartType
---

# IPart::GetPartType


## -description

The <b>GetPartType</b> method gets the part type of this part.

## -parameters

### -param pPartType [out]

Pointer to a <a href="/windows/win32/api/devicetopology/ne-devicetopology-parttype">PartType</a> variable into which the method writes the part type. The part type is one of the following <b>PartType</b> enumeration values, which indicate whether the part is a connector or subunit:

Connector

Subunit

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
Pointer <i>pPartType</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

For a code example that uses this method, see the implementation of the SelectCaptureDevice function in <a href="/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>