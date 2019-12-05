---
UID: NF:mfidl.IMFSensorActivitiesReport.GetActivityReportByDeviceName
title: IMFSensorActivitiesReport::GetActivityReportByDeviceName (mfidl.h)
description: Retrieves an IMFSensorActivityReport based on the specified device name.
old-location: mf\imfsensoractivityreport_getactivityreportbydevicename.htm
tech.root: medfound
ms.assetid: 66FDBCE0-E3F3-43A4-B34A-7FE6C7F3F918
ms.date: 12/05/2018
ms.keywords: GetActivityReportByDeviceName, GetActivityReportByDeviceName method [Media Foundation], GetActivityReportByDeviceName method [Media Foundation],IMFSensorActivitiesReport interface, IMFSensorActivitiesReport interface [Media Foundation],GetActivityReportByDeviceName method, IMFSensorActivitiesReport.GetActivityReportByDeviceName, IMFSensorActivitiesReport::GetActivityReportByDeviceName, mf.imfsensoractivityreport_getactivityreportbydevicename, mfidl/IMFSensorActivitiesReport::GetActivityReportByDeviceName
ms.topic: method
f1_keywords:
- mfidl/IMFSensorActivitiesReport.GetActivityReportByDeviceName
dev_langs:
- c++
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
- IMFSensorActivitiesReport.GetActivityReportByDeviceName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSensorActivitiesReport::GetActivityReportByDeviceName


## -description


Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport">IMFSensorActivityReport</a> based on the specified device name.


## -parameters




### -param SymbolicName

The symbolic name of the sensor for which the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport">IMFSensorActivityReport</a> is retrieved. 


### -param sensorActivityReport [out]

A pointer to the  <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport">IMFSensorActivityReport</a> associated with the sensor with the specified symbolic name.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>symbolicName</i> parameter is null.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDINDEX</b></dt>
</dl>
</td>
<td width="60%">
The <i>Index</i> parameter is not less than value returned by <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensoractivitiesreport-getcount">GetCount</a>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No sensor with the specified symbolic name was found.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreport">IMFSensorActivitiesReport</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport">IMFSensorActivityReport</a>
 

 

