---
UID: NF:mfidl.IMFSensorActivityReport.GetSymbolicLink
title: IMFSensorActivityReport::GetSymbolicLink (mfidl.h)
description: Gets the symbolic link for the sensor associated with the report.
helpviewer_keywords: ["GetSymbolicLink","GetSymbolicLink method [Media Foundation]","GetSymbolicLink method [Media Foundation]","IMFSensorActivityReport interface","IMFSensorActivityReport interface [Media Foundation]","GetSymbolicLink method","IMFSensorActivityReport.GetSymbolicLink","IMFSensorActivityReport::GetSymbolicLink","mf.imfsensoractivityreport_getsymboliclink","mfidl/IMFSensorActivityReport::GetSymbolicLink"]
old-location: mf\imfsensoractivityreport_getsymboliclink.htm
tech.root: mf
ms.assetid: BF0BDB21-DE87-4177-A94F-8BA8FD571B02
ms.date: 12/05/2018
ms.keywords: GetSymbolicLink, GetSymbolicLink method [Media Foundation], GetSymbolicLink method [Media Foundation],IMFSensorActivityReport interface, IMFSensorActivityReport interface [Media Foundation],GetSymbolicLink method, IMFSensorActivityReport.GetSymbolicLink, IMFSensorActivityReport::GetSymbolicLink, mf.imfsensoractivityreport_getsymboliclink, mfidl/IMFSensorActivityReport::GetSymbolicLink
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
 - IMFSensorActivityReport::GetSymbolicLink
 - mfidl/IMFSensorActivityReport::GetSymbolicLink
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
 - IMFSensorActivityReport.GetSymbolicLink
---

# IMFSensorActivityReport::GetSymbolicLink


## -description

Gets the symbolic link for the sensor associated with the report.

## -parameters

### -param SymbolicLink [out]

The string into which the sensor symbolic link is written.

### -param cchSymbolicLink [in]

The character count of the <i>SymbolicLink</i> string.

### -param pcchWritten [in, out]

Receives the number of characters that were written into the <i>SymbolicLink</i> string.

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
The <i>pcchWritten</i> parameter is null.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport">IMFSensorActivityReport</a>