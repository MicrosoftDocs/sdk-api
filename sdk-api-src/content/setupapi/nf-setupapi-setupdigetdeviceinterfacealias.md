---
UID: NF:setupapi.SetupDiGetDeviceInterfaceAlias
title: SetupDiGetDeviceInterfaceAlias function
author: windows-sdk-content
description: The SetupDiGetDeviceInterfaceAlias function returns an alias of a specified device interface.
old-location: devinst\setupdigetdeviceinterfacealias.htm
old-project: devinst
ms.assetid: eb36da2a-4ff1-4f2b-abc6-9bdaf491252f
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: SetupDiGetDeviceInterfaceAlias, SetupDiGetDeviceInterfaceAlias function [Device and Driver Installation], devinst.setupdigetdeviceinterfacealias, di-rtns_a9f0fc2b-7a4e-49fc-afc5-723a0120a5d7.xml, setupapi/SetupDiGetDeviceInterfaceAlias
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
 - SetupDiGetDeviceInterfaceAlias
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupDiGetDeviceInterfaceAlias function


## -description


The <b>SetupDiGetDeviceInterfaceAlias</b> function returns an alias of a specified device interface. 


## -parameters




### -param DeviceInfoSet [in]

A pointer to the <a href="devinst.device_information_sets">device information set</a> that contains the device interface for which to retrieve an alias. This handle is typically returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff551069">SetupDiGetClassDevs</a>.


### -param DeviceInterfaceData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552342">SP_DEVICE_INTERFACE_DATA</a> structure that specifies the device interface in <i>DeviceInfoSet</i> for which to retrieve an alias. This pointer is typically returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff551015">SetupDiEnumDeviceInterfaces</a>.


### -param AliasInterfaceClassGuid [in]

A pointer to a GUID that specifies the interface class of the alias to retrieve.


### -param AliasDeviceInterfaceData [out]

A pointer to a caller-allocated buffer that contains, on successful return, a completed <a href="https://msdn.microsoft.com/library/windows/hardware/ff552342">SP_DEVICE_INTERFACE_DATA</a> structure that identifies the requested alias. The caller must set <i>AliasDeviceInterfaceData</i><b>.cbSize</b> to <b>sizeof</b>(SP_DEVICE_INTERFACE_DATA) before calling this function. 


## -returns



<b>SetupDiGetDeviceInterfaceAlias</b> returns <b>TRUE</b> if the function completed without error. If the function completed with an error, <b>FALSE</b> is returned and the error code for the failure can be retrieved by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.

Possible errors returned by <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> are listed in the following table.


<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Invalid <i>DeviceInfoSet</i> or invalid <i>DeviceInterfaceData</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_INTERFACE_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
There is no alias of class <i>AliasInterfaceClassGuid</i> for the specified device interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_USER_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Invalid <i>AliasDeviceInterfaceData</i> buffer. 

</td>
</tr>
</table>
 




## -remarks



Device interfaces are considered aliases if they are of different interface classes but are supported by the same device and have identical reference strings.

<b>SetupDiGetDeviceInterfaceAlias</b> can be used to locate a device that exposes more than one interface. For example, consider a disk that can be part of a fault-tolerant volume and can contain encrypted data. The function driver for the disk device could register a fault-tolerant-volume interface and an encrypted-volume interface. These interfaces are device interface aliases if the function driver registers them with identical reference strings and they refer to the same device. (The reference strings will likely be <b>NULL</b> and therefore are equal.)

To locate such a multi-interface device, first locate all available devices that expose one of the interfaces, such as the fault-tolerant-volume interface, using <a href="https://msdn.microsoft.com/library/windows/hardware/ff551069">SetupDiGetClassDevs</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff551015">SetupDiEnumDeviceInterfaces</a>. Then, pass a device with the first interface (fault-tolerant-volume) to <b>SetupDiGetDeviceInterfaceAlias</b> and request an alias of the other interface class (encrypted-volume). 

If the requested alias exists but the caller-supplied <i>AliasDeviceInterfaceData</i> buffer is invalid, this function successfully adds the device interface element to <i>DevInfoSet</i> but returns <b>FALSE</b> for the return value. In this case, <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_INVALID_USER_BUFFER.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551015">SetupDiEnumDeviceInterfaces</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551069">SetupDiGetClassDevs</a>
 

 

