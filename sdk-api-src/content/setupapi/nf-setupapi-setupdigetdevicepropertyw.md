---
UID: NF:setupapi.SetupDiGetDevicePropertyW
title: SetupDiGetDevicePropertyW function
author: windows-sdk-content
description: The SetupDiGetDeviceProperty function retrieves a device instance property.
old-location: devinst\setupdigetdeviceproperty.htm
old-project: devinst
ms.assetid: eac31612-e80b-44ad-b4d4-a4aa014e833f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetupDiGetDeviceProperty, SetupDiGetDeviceProperty function [Device and Driver Installation], SetupDiGetDevicePropertyW, devinst.setupdigetdeviceproperty, di-rtns_e079700c-c7b8-43ef-992b-68156a693b41.xml, setupapi/SetupDiGetDeviceProperty, setupapi/SetupDiGetDevicePropertyW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: SetupAPI.h
req.redist: 
req.target-type: DesktopFor universal, call CM_Get_DevNode_Property
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupDiGetDevicePropertyW (Unicode)
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
 - SetupAPI.dll
 - ext-ms-win-setupapi-classinstallers-l1-1-0.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-1.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupDiGetDeviceProperty
 - SetupDiGetDevicePropertyW
product: Windows
targetos: Windows
req.lib: SetupAPI.lib
req.dll: SetupAPI.dll
req.irql: 
req.product: ADAM
---

# SetupDiGetDevicePropertyW function


## -description


The <b>SetupDiGetDeviceProperty</b> function retrieves a device instance property.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="https://msdn.microsoft.com/library/Ff541247(v=VS.85).aspx">device information set</a> that contains a device instance for which to retrieve a device instance property.


### -param DeviceInfoData [in]

A pointer to the <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that represents the device instance for which to retrieve a device instance property.


### -param PropertyKey [in]

A pointer to a <a href="https://msdn.microsoft.com/98986d43-84c0-44e6-83f9-08e872ea5e6d">DEVPROPKEY</a> structure that represents the device property key of the requested device instance property.


### -param PropertyType [out]

A pointer to a <a href="https://msdn.microsoft.com/e0fdcc28-be70-4ae1-bd6d-89e2177eae62">DEVPROPTYPE</a>-typed variable that receives the property-data-type identifier of the requested device instance property, where the property-data-type identifier is the bitwise OR between a base-data-type identifier and, if the base-data type is modified, a property-data-type modifier.


### -param PropertyBuffer [out, optional]

A pointer to a buffer that receives the requested device instance property. <b>SetupDiGetDeviceProperty</b> retrieves the requested property only if the buffer is large enough to hold all the property value data. The pointer can be <b>NULL</b>. If the pointer is set to <b>NULL</b> and <i>RequiredSize</i> is supplied, <b>SetupDiGetDeviceProperty</b> returns the size of the property, in bytes, in *<i>RequiredSize</i>.


### -param PropertyBufferSize [in]

The size, in bytes, of the <i>PropertyBuffer</i> buffer. If <i>PropertyBuffer</i> is set to <b>NULL</b>, <i>PropertyBufferSize</i> must be set to zero.


### -param RequiredSize [out, optional]

A pointer to a DWORD-typed variable that receives the size, in bytes, of either the device instance property if the property is retrieved or the required buffer size if the buffer is not large enough. This pointer can be set to <b>NULL</b>.


### -param Flags [in]

This parameter must be set to zero.


## -returns



<b>SetupDiGetDeviceProperty</b> returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b>, and the logged error can be retrieved by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.

The following table includes some of the more common error codes that this function might log.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The value of<i> Flags</i> is not zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The device information set that is specified by <i>DevInfoSet</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A supplied parameter is not valid. One possibility is that the device information element is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_REG_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The property key that is supplied by <i>PropertyKey</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
An unspecified internal data value was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_USER_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
A user buffer is not valid. One possibility is that <i>PropertyBuffer</i> is <b>NULL</b> and <i>PropertBufferSize</i> is not zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_DEVINST</b></dt>
</dl>
</td>
<td width="60%">
The device instance that is specified by <i>DevInfoData</i> does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>PropertyBuffer</i> buffer is too small to hold the requested property value, or an internal data buffer that was passed to a system call was too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough system memory available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The requested device property does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have Administrator privileges.

</td>
</tr>
</table>
 




## -remarks



<b>SetupDiGetDeviceProperty</b> is part of the <a href="https://msdn.microsoft.com/library/Ff553515(v=VS.85).aspx">unified device property model</a>.

SetupAPI supports only a Unicode version of <b>SetupDiGetDeviceProperty</b>.

To obtain the device property keys that represent the device properties that are set for a device instance, call <a href="https://msdn.microsoft.com/d4decdab-e412-4719-ad65-74f34cf8df27">SetupDiGetDevicePropertyKeys</a>.

To set a device instance property, call <a href="https://msdn.microsoft.com/c03c51ba-3027-4be9-8869-6d7dbeac2428">SetupDiSetDeviceProperty</a>.




## -see-also




<a href="https://msdn.microsoft.com/d4decdab-e412-4719-ad65-74f34cf8df27">SetupDiGetDevicePropertyKeys</a>



<a href="https://msdn.microsoft.com/c03c51ba-3027-4be9-8869-6d7dbeac2428">SetupDiSetDeviceProperty</a>
 

 

