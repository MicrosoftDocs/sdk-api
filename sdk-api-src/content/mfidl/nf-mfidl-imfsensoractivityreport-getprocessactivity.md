---
UID: NF:mfidl.IMFSensorActivityReport.GetProcessActivity
title: IMFSensorActivityReport::GetProcessActivity (mfidl.h)
description: Gets an IMFSensorProcessActivity object representing the current process activity of a sensor.
helpviewer_keywords: ["GetProcessActivity","GetProcessActivity method [Media Foundation]","GetProcessActivity method [Media Foundation]","IMFSensorActivityReport interface","IMFSensorActivityReport interface [Media Foundation]","GetProcessActivity method","IMFSensorActivityReport.GetProcessActivity","IMFSensorActivityReport::GetProcessActivity","mf.imfsensoractivityreport_getprocessactivity","mfidl/IMFSensorActivityReport::GetProcessActivity"]
old-location: mf\imfsensoractivityreport_getprocessactivity.htm
tech.root: mf
ms.assetid: A9E18EC3-83E4-430B-B7A4-49FC9736A94E
ms.date: 12/05/2018
ms.keywords: GetProcessActivity, GetProcessActivity method [Media Foundation], GetProcessActivity method [Media Foundation],IMFSensorActivityReport interface, IMFSensorActivityReport interface [Media Foundation],GetProcessActivity method, IMFSensorActivityReport.GetProcessActivity, IMFSensorActivityReport::GetProcessActivity, mf.imfsensoractivityreport_getprocessactivity, mfidl/IMFSensorActivityReport::GetProcessActivity
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
 - IMFSensorActivityReport::GetProcessActivity
 - mfidl/IMFSensorActivityReport::GetProcessActivity
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
 - IMFSensorActivityReport.GetProcessActivity
---

# IMFSensorActivityReport::GetProcessActivity


## -description

Gets an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprocessactivity">IMFSensorProcessActivity</a> object representing the current process activity of a sensor.

## -parameters

### -param Index [in]

The index of the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprocessactivity">IMFSensorProcessActivity</a> to retrieve. This value must be less than the value returned by <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsensoractivityreport-getprocesscount">GetProcessCount</a>.

### -param ppProcessActivity [in]

 A pointer to the  <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprocessactivity">IMFSensorProcessActivity</a> associated with the specified index.

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
The <i>ppProcessActivity</i> parameter is null.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport">IMFSensorActivityReport</a>