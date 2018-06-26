---
UID: NF:setupapi.SetupDiLoadDeviceIcon
title: SetupDiLoadDeviceIcon function
author: windows-sdk-content
description: The SetupDiLoadDeviceIcon function retrieves an icon for a specified device.
old-location: devinst\setupdiloaddeviceicon.htm
old-project: devinst
ms.assetid: 65a47cea-1c70-46ed-9cf5-601387dbe323
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: SetupDiLoadDeviceIcon, SetupDiLoadDeviceIcon function [Device and Driver Installation], devinst.setupdiloaddeviceicon, di-rtns_bcd13849-30ed-4c7e-923d-1524552d78aa.xml, setupapi/SetupDiLoadDeviceIcon
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
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
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupDiLoadDeviceIcon
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupDiLoadDeviceIcon function


## -description


The <b>SetupDiLoadDeviceIcon</b> function retrieves an icon for a specified device.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> that contains the device information element that represents the device for which to retrieve an icon. 


### -param DeviceInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. 


### -param cxIcon [in]

The width, in pixels, of the icon to be retrieved. Use the system metric index SM_CXICON to specify a default-sized icon or use the system metric index SM_CXSMICON to specify a small icon. The system metric indexes are defined in <i>Winuser.h</i>, and their associated values can be retrieved by a call to the <a href="http://go.microsoft.com/fwlink/p/?linkid=74034">GetSystemMetrics</a> function. (The <b>GetSystemMetrics</b> function is documented in the Microsoft Windows SDK.)


### -param cyIcon [in]

The height, in pixels, of the icon to be retrieved. Use SM_CXICON to specify a default-sized icon or use SM_CXSMICON to specify a small icon.


### -param Flags [in]

Not used. Must set to zero.


### -param hIcon [out]

A pointer to a handle to an icon that receives a handle to the icon that this function retrieves. After the application that calls this function is finished using the icon, the application must call <a href="http://go.microsoft.com/fwlink/p/?linkid=74035">DestroyIcon</a> to delete the icon. (<b>DestroyIcon</b> is documented in the Microsoft Windows SDK.)


## -returns



<b>SetupDiLoadDeviceIcon</b> returns <b>TRUE</b> if the function succeeds in retrieving the icon for the specified device. Otherwise, the function returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=74036">GetLastError</a>. 




## -remarks



<b>SetupDiLoadDeviceIcon</b> attempts to retrieve an icon for the device as follows: 

<ul>
<li>
If the <a href="https://msdn.microsoft.com/library/windows/hardware/ff543520">DEVPKEY_DrvPkg_Icon</a> device property of the device includes a list of resource-identifier strings, the function attempts to retrieve the icon that is specified by the first resource-identifier string in the list. 

The <a href="https://msdn.microsoft.com/eafe72c3-b9d8-44c4-a8a7-45a7e0d19b4e">device property data type</a> of the DEVPKEY_DrvPkg_Icon device property is <a href="https://msdn.microsoft.com/library/windows/hardware/ff543614">DEVPROP_TYPE_STRING_LIST</a>. 

The format of a resource-identifier string is

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>[filepath\]filename,-resourceID</pre>
</td>
</tr>
</table></span></div>
Where:

<ul>
<li><i>filepath,</i> followed by the backslash character ("\")<i>,</i> is optional and specifies a path of the file that contains the icon.</li>
<li><i>FileName</i>, followed by the comma character (",") specifies the name of the file that contains the icon.</li>
<li><i>ResourceID</i>, preceded by a dash character ("-"), specifies the resource ID of the icon.</li>
</ul>
</li>
<li>
If the function cannot retrieve a device-specific icon, it will then attempt to retrieve the class icon for the device. For information about class icons, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff552053">SetupDiLoadClassIcon</a>.

</li>
<li>
If the function cannot retrieve the class icon for the device, it will then attempt to retrieve the icon for the Unknown <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a>, where the icon for the Unknown device setup class includes the image of a question mark (?).

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543614">DEVPROP_TYPE_STRING_LIST</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552053">SetupDiLoadClassIcon</a>
 

 

