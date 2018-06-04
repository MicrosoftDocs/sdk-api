---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# SerialDisplayAdvancedSettings function


## -description


<b>SerialDisplayAdvancedSettings</b> displays the system-supplied advanced settings dialog box for a specified COM port device.


## -parameters




### -param ParentHwnd [in]

Handle to the parent window for the advanced settings dialog box.


### -param DeviceInfoSet [in]

Specifies the device information set that includes the device instance specified by <i>DeviceInfoData</i>.


### -param DeviceInfoData [in]

Pointer to the device instance in the specified device information set. The routine displays the advanced settings dialog box for this device.


## -returns



<b>SerialDisplayAdvancedSettings</b> returns one of the following status values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The advanced settings dialog box was successfully displayed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the following occurred: The specified device information set is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The routine could not open the specified device's hardware registry key.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The name of the port is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The routine could not display the dialog box.

</td>
</tr>
</table>
 




## -remarks



<b>SerialDisplayAdvancedSettings</b> displays the system-supplied advanced settings dialog box for a specified device. If you supply a custom dialog box, this routine displays it; otherwise, the routine displays the default dialog box.

<b>SerialDisplayAdvancedSettings</b> runs in user mode.

For more information, see <a href="https://msdn.microsoft.com/056fd245-a9d2-4a10-9e92-fe75e51f6770">Installing an Advanced Properties Page for a COM Port</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546956">PPORT_ADVANCED_DIALOG</a>
 

 

