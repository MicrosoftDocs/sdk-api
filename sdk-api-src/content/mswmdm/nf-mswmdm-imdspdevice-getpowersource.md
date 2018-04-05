---
UID: NF:mswmdm.IMDSPDevice.GetPowerSource
title: IMDSPDevice::GetPowerSource method
author: windows-driver-content
description: The GetPowerSource method reports whether the device is capable of running on batteries, external power, or both, and on which type of power source it is currently running.
old-location: wmdm\imdspdevice_getpowersource.htm
old-project: WMDM
ms.assetid: 476e25cf-de18-4039-994c-570fa423821f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetPowerSource method [windows Media Device Manager], GetPowerSource method [windows Media Device Manager], IMDSPDevice interface, GetPowerSource,IMDSPDevice.GetPowerSource, IMDSPDevice, IMDSPDevice interface [windows Media Device Manager], GetPowerSource method, IMDSPDevice::GetPowerSource, IMDSPDeviceGetPowerSource, mswmdm/IMDSPDevice::GetPowerSource, wmdm.imdspdevice_getpowersource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IMDSPDevice.GetPowerSource
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMDSPDevice::GetPowerSource method


## -description



The <b>GetPowerSource</b> method reports whether the device is capable of running on batteries, external power, or both, and on which type of power source it is currently running. If the device is running on batteries, this method also reports the percentage of total power remaining in the batteries.




## -parameters




### -param pdwPowerSource [out]

Pointer to a <b>DWORD</b> that receives a value indicating the current power source for the device. The value is one of the following flags.

<table>
<tr>
<th>
                  Flag
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>WMDM_POWER_CAP_BATTERY</td>
<td>The media device can run on batteries.</td>
</tr>
<tr>
<td>WMDM_POWER_CAP_EXTERNAL</td>
<td>The media device can run on external power.</td>
</tr>
<tr>
<td>WMDM_POWER_IS_BATTERY</td>
<td>The media device is currently running on batteries.</td>
</tr>
<tr>
<td>WMDM_POWER_IS_EXTERNAL</td>
<td>The media device is currently running on external power.</td>
</tr>
<tr>
<td>WMDM_POWER_PERCENT_AVAILABLE</td>
<td>The percentage of power remaining was returned in <i>pdwPercentRemaining</i>.</td>
</tr>
</table>
 


### -param pdwPercentRemaining [out]

If the device is running on batteries, <i>pdwPercentRemaining</i> specifies a pointer to a <b>DWORD</b> containing the percentage of total battery power remaining.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



Only physical devices report power source capabilities and current power source. Software implementations of devices report no power capabilities or current power source.

This method is optional. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice Interface</a>
 

 

