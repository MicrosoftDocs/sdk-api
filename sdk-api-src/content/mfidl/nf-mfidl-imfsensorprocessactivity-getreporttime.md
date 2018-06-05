---
UID: NF:mfidl.IMFSensorProcessActivity.GetReportTime
title: IMFSensorProcessActivity::GetReportTime
author: windows-sdk-content
description: Gets the time associated with the sensor activity report.
old-location: mf\imfsensorprocessactivity_getreporttime.htm
old-project: medfound
ms.assetid: 5C13F0ED-B2A6-43AC-92AA-87BF995DEFD7
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetReportTime, GetReportTime method [Media Foundation], GetReportTime method [Media Foundation],IMFSensorProcessActivity interface, IMFSensorProcessActivity interface [Media Foundation],GetReportTime method, IMFSensorProcessActivity.GetReportTime, IMFSensorProcessActivity::GetReportTime, mf.imfsensorprocessactivity_getreporttime, mfidl/IMFSensorProcessActivity::GetReportTime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfplat.lib
-	mfplat.dll
-	mfplat.dll
-	mfplat.dll.dll
api_name:
-	IMFSensorProcessActivity.GetReportTime
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorProcessActivity::GetReportTime


## -description


Gets the time associated with the sensor activity report.


## -parameters




### -param pft [out]

Receives the time associated with the sensor activity report.


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
The <i>pft</i> parameter is null.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/833A24EA-11E0-47CF-A710-06E38A1FD50A">IMFSensorProcessActivity</a>
 

 

