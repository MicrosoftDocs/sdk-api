---
UID: NF:mfidl.IMFSensorActivitiesReport.GetActivityReport
title: IMFSensorActivitiesReport::GetActivityReport
author: windows-sdk-content
description: Retrieves an IMFSensorActivityReport based on the specified index.
old-location: mf\imfsensoractivityreport_getactivityreport.htm
old-project: medfound
ms.assetid: 6E8D7039-9CBF-45A0-8CAE-48F79091D40B
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetActivityReport, GetActivityReport method [Media Foundation], GetActivityReport method [Media Foundation],IMFSensorActivitiesReport interface, IMFSensorActivitiesReport interface [Media Foundation],GetActivityReport method, IMFSensorActivitiesReport.GetActivityReport, IMFSensorActivitiesReport::GetActivityReport, mf.imfsensoractivityreport_getactivityreport, mfidl/IMFSensorActivitiesReport::GetActivityReport
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
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorActivitiesReport::GetActivityReport


## -description


Retrieves an <a href="https://msdn.microsoft.com/06612B8E-5C1E-487C-B6EF-15F65DEA27D0">IMFSensorActivityReport</a> based on the specified index.


## -parameters




### -param Index [in]

The index of the <a href="https://msdn.microsoft.com/06612B8E-5C1E-487C-B6EF-15F65DEA27D0">IMFSensorActivityReport</a> to retrieve. This value must be less than the value returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>. 


### -param sensorActivityReport [out]

A pointer to the  <a href="https://msdn.microsoft.com/06612B8E-5C1E-487C-B6EF-15F65DEA27D0">IMFSensorActivityReport</a> associated with the specified index.


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
The <i>Index</i> parameter is not less than value returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>. 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/CECDE9D5-B5D4-4DF3-80A8-F4B0B37CC5C3">IMFSensorActivitiesReport</a>



<a href="https://msdn.microsoft.com/06612B8E-5C1E-487C-B6EF-15F65DEA27D0">IMFSensorActivityReport</a>
 

 

