---
UID: NF:mfidl.IMFSensorGroup.GetFlags
title: IMFSensorGroup::GetFlags (mfidl.h)
description: Gets the flags set for the sensor group.
helpviewer_keywords: ["GetFlags","GetFlags method [Media Foundation]","GetFlags method [Media Foundation]","IMFSensorGroup interface","IMFSensorGroup interface [Media Foundation]","GetFlags method","IMFSensorGroup.GetFlags","IMFSensorGroup::GetFlags","mf.imfsensorgroup_getflags","mfidl/IMFSensorGroup::GetFlags"]
old-location: mf\imfsensorgroup_getflags.htm
tech.root: mf
ms.assetid: 99143CFD-930A-405C-A8FB-8DBF52CD9BB5
ms.date: 12/05/2018
ms.keywords: GetFlags, GetFlags method [Media Foundation], GetFlags method [Media Foundation],IMFSensorGroup interface, IMFSensorGroup interface [Media Foundation],GetFlags method, IMFSensorGroup.GetFlags, IMFSensorGroup::GetFlags, mf.imfsensorgroup_getflags, mfidl/IMFSensorGroup::GetFlags
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSensorGroup::GetFlags
 - mfidl/IMFSensorGroup::GetFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorGroup.GetFlags
---

# IMFSensorGroup::GetFlags


## -description

Gets the flags set for the sensor group.

## -parameters

### -param pFlags [out]

The flags set for the sensor group

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The sensor group has not been initialized.

</td>
</tr>
</table>

## -remarks

Currently, no flags are defined for Sensor Groups.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup">IMFSensorGroup</a>