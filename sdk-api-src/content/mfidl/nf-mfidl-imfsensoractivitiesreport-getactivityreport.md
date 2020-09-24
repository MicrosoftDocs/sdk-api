---
UID: NF:mfidl.IMFSensorActivitiesReport.GetActivityReport
title: IMFSensorActivitiesReport::GetActivityReport (mfidl.h)
description: Retrieves an IMFSensorActivityReport based on the specified index.
helpviewer_keywords: ["GetActivityReport","GetActivityReport method [Media Foundation]","GetActivityReport method [Media Foundation]","IMFSensorActivitiesReport interface","IMFSensorActivitiesReport interface [Media Foundation]","GetActivityReport method","IMFSensorActivitiesReport.GetActivityReport","IMFSensorActivitiesReport::GetActivityReport","mf.imfsensoractivityreport_getactivityreport","mfidl/IMFSensorActivitiesReport::GetActivityReport"]
old-location: mf\imfsensoractivityreport_getactivityreport.htm
tech.root: mf
ms.assetid: 6E8D7039-9CBF-45A0-8CAE-48F79091D40B
ms.date: 12/05/2018
ms.keywords: GetActivityReport, GetActivityReport method [Media Foundation], GetActivityReport method [Media Foundation],IMFSensorActivitiesReport interface, IMFSensorActivitiesReport interface [Media Foundation],GetActivityReport method, IMFSensorActivitiesReport.GetActivityReport, IMFSensorActivitiesReport::GetActivityReport, mf.imfsensoractivityreport_getactivityreport, mfidl/IMFSensorActivitiesReport::GetActivityReport
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
 - IMFSensorActivitiesReport::GetActivityReport
 - mfidl/IMFSensorActivitiesReport::GetActivityReport
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
 - IMFSensorActivitiesReport.GetActivityReport
---

# IMFSensorActivitiesReport::GetActivityReport


## -description

Retrieves an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport">IMFSensorActivityReport</a> based on the specified index.

## -parameters

### -param Index [in]

The index of the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport">IMFSensorActivityReport</a> to retrieve. This value must be less than the value returned by <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsensoractivitiesreport-getcount">GetCount</a>.

### -param sensorActivityReport [out]

A pointer to the  <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport">IMFSensorActivityReport</a> associated with the specified index.

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
The <i>sensorActivityReport</i> parameter is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDINDEX</b></dt>
</dl>
</td>
<td width="60%">
The <i>Index</i> parameter is not less than value returned by <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsensoractivitiesreport-getcount">GetCount</a>. 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreport">IMFSensorActivitiesReport</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport">IMFSensorActivityReport</a>