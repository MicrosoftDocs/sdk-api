---
UID: NF:mfidl.IMFSensorProcessActivity.GetProcessId
title: IMFSensorProcessActivity::GetProcessId (mfidl.h)
description: Gets the ID of the process with which the activity is associated.
helpviewer_keywords: ["GetProcessId","GetProcessId method [Media Foundation]","GetProcessId method [Media Foundation]","IMFSensorProcessActivity interface","IMFSensorProcessActivity interface [Media Foundation]","GetProcessId method","IMFSensorProcessActivity.GetProcessId","IMFSensorProcessActivity::GetProcessId","mf.imfsensorprocessactivity_getprocessid","mfidl/IMFSensorProcessActivity::GetProcessId"]
old-location: mf\imfsensorprocessactivity_getprocessid.htm
tech.root: mf
ms.assetid: E4277F4B-8CBB-4910-991B-1234AFEB49B3
ms.date: 12/05/2018
ms.keywords: GetProcessId, GetProcessId method [Media Foundation], GetProcessId method [Media Foundation],IMFSensorProcessActivity interface, IMFSensorProcessActivity interface [Media Foundation],GetProcessId method, IMFSensorProcessActivity.GetProcessId, IMFSensorProcessActivity::GetProcessId, mf.imfsensorprocessactivity_getprocessid, mfidl/IMFSensorProcessActivity::GetProcessId
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
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
 - IMFSensorProcessActivity::GetProcessId
 - mfidl/IMFSensorProcessActivity::GetProcessId
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
 - IMFSensorProcessActivity.GetProcessId
---

# IMFSensorProcessActivity::GetProcessId


## -description

Gets the ID of the process with which the activity is associated.

## -parameters

### -param pPID [out]

Receives the process ID.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pPID</i> parameter is null.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprocessactivity">IMFSensorProcessActivity</a>