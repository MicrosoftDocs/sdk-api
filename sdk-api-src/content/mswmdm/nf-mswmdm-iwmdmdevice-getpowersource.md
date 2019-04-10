---
UID: NF:mswmdm.IWMDMDevice.GetPowerSource
title: IWMDMDevice::GetPowerSource (mswmdm.h)
author: windows-sdk-content
description: The GetPowerSource method retrieves information about the power source and the percentage of power remaining for the device.
old-location: wmdm\iwmdmdevice_getpowersource.htm
tech.root: WMDM
ms.assetid: 0e13ac64-69b7-4c44-8690-8fcef6cb354f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPowerSource, GetPowerSource method [windows Media Device Manager], GetPowerSource method [windows Media Device Manager],IWMDMDevice interface, IWMDMDevice interface [windows Media Device Manager],GetPowerSource method, IWMDMDevice.GetPowerSource, IWMDMDevice::GetPowerSource, IWMDMDeviceGetPowerSource, mswmdm/IWMDMDevice::GetPowerSource, wmdm.iwmdmdevice_getpowersource
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMDevice.GetPowerSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMDevice::GetPowerSource


## -description



The <b>GetPowerSource</b> method retrieves information about the power source and the percentage of power remaining for the device.




## -parameters




### -param pdwPowerSource [out]

Pointer to a <b>DWORD</b> specifying information about the power source of the device.

The possible returned values are a bitwise <b>OR</b> of one or more of the following values.

<table>
<tr>
<th>Flag
                </th>
<th>Description
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

If <i>pdwPowerSource</i> contains WMDM_POWER_PERCENT_AVAILABLE, a pointer to a <b>DWORD</b> specifying the percentage of power remaining in the device.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/44212da9-a38a-4ed5-86af-cf60b40bb54d">IWMDMDevice Interface</a>
 

 

