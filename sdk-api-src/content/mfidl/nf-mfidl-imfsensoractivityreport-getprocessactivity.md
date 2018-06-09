---
UID: NF:mfidl.IMFSensorActivityReport.GetProcessActivity
title: IMFSensorActivityReport::GetProcessActivity
author: windows-sdk-content
description: Gets an IMFSensorProcessActivity object representing the current process activity of a sensor.
old-location: mf\imfsensoractivityreport_getprocessactivity.htm
old-project: medfound
ms.assetid: A9E18EC3-83E4-430B-B7A4-49FC9736A94E
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetProcessActivity, GetProcessActivity method [Media Foundation], GetProcessActivity method [Media Foundation],IMFSensorActivityReport interface, IMFSensorActivityReport interface [Media Foundation],GetProcessActivity method, IMFSensorActivityReport.GetProcessActivity, IMFSensorActivityReport::GetProcessActivity, mf.imfsensoractivityreport_getprocessactivity, mfidl/IMFSensorActivityReport::GetProcessActivity
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
 - IMFSensorActivityReport.GetProcessActivity
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorActivityReport::GetProcessActivity


## -description


Gets an <a href="https://msdn.microsoft.com/833A24EA-11E0-47CF-A710-06E38A1FD50A">IMFSensorProcessActivity</a> object representing the current process activity of a sensor.


## -parameters




### -param Index [in]

The index of the <a href="https://msdn.microsoft.com/833A24EA-11E0-47CF-A710-06E38A1FD50A">IMFSensorProcessActivity</a> to retrieve. This value must be less than the value returned by <a href="https://msdn.microsoft.com/9C3DAB31-9D28-42CB-AFB8-6288658FF6B0">GetProcessCount</a>. 


### -param ppProcessActivity [in]

 A pointer to the  <a href="https://msdn.microsoft.com/833A24EA-11E0-47CF-A710-06E38A1FD50A">IMFSensorProcessActivity</a> associated with the specified index.


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




<a href="https://msdn.microsoft.com/06612B8E-5C1E-487C-B6EF-15F65DEA27D0">IMFSensorActivityReport</a>
 

 

