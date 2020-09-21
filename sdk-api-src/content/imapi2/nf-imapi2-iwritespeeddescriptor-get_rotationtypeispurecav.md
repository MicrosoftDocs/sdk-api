---
UID: NF:imapi2.IWriteSpeedDescriptor.get_RotationTypeIsPureCAV
title: IWriteSpeedDescriptor::get_RotationTypeIsPureCAV (imapi2.h)
description: Retrieves the supported rotational-speed control used by the recorder for the current media.
helpviewer_keywords: ["IWriteSpeedDescriptor interface [IMAPI]","get_RotationTypeIsPureCAV method","IWriteSpeedDescriptor.get_RotationTypeIsPureCAV","IWriteSpeedDescriptor::get_RotationTypeIsPureCAV","get_RotationTypeIsPureCAV","get_RotationTypeIsPureCAV method [IMAPI]","get_RotationTypeIsPureCAV method [IMAPI]","IWriteSpeedDescriptor interface","imapi.iwritespeeddescriptor_get_rotationtypeispurecav","imapi2/IWriteSpeedDescriptor::get_RotationTypeIsPureCAV"]
old-location: imapi\iwritespeeddescriptor_get_rotationtypeispurecav.htm
tech.root: imapi
ms.assetid: 36c509a2-6592-4fa0-8e4a-4b21f4cf7a13
ms.date: 12/05/2018
ms.keywords: IWriteSpeedDescriptor interface [IMAPI],get_RotationTypeIsPureCAV method, IWriteSpeedDescriptor.get_RotationTypeIsPureCAV, IWriteSpeedDescriptor::get_RotationTypeIsPureCAV, get_RotationTypeIsPureCAV, get_RotationTypeIsPureCAV method [IMAPI], get_RotationTypeIsPureCAV method [IMAPI],IWriteSpeedDescriptor interface, imapi.iwritespeeddescriptor_get_rotationtypeispurecav, imapi2/IWriteSpeedDescriptor::get_RotationTypeIsPureCAV
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IWriteSpeedDescriptor::get_RotationTypeIsPureCAV
 - imapi2/IWriteSpeedDescriptor::get_RotationTypeIsPureCAV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IWriteSpeedDescriptor.get_RotationTypeIsPureCAV
---

# IWriteSpeedDescriptor::get_RotationTypeIsPureCAV


## -description

Retrieves the supported rotational-speed control used by the recorder for the current media.

## -parameters

### -param value [out]

Is VARIANT_TRUE if constant angular velocity (CAV)  rotational-speed control is in use. Otherwise, VARIANT_FALSE to indicate that another rotational-speed control that the recorder supports is in use.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

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
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>

## -remarks

Rotational-speed control types include the following:

<ul>
<li>	CLV (Constant Linear Velocity). The disc is written at a constant speed. Standard rotational control.</li>
<li>	CAV (Constant Angular Velocity). The disc is written at a constantly increasing speed.</li>
<li>	ZCAV (Zone Constant Linear Velocity). The disc is divided into zones. After each zone, the write speed increases. This is an impure form of CAV.</li>
<li>	PCAV (Partial Constant Angular Velocity). The disc speed increases up to a specified velocity. Once reached, the disc spins at the specified velocity for the duration of the disc writing.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor">IWriteSpeedDescriptor</a>