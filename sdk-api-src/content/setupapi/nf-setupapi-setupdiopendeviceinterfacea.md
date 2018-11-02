---
UID: NF:setupapi.SetupDiOpenDeviceInterfaceA
title: SetupDiOpenDeviceInterfaceA function
author: windows-sdk-content
description: The SetupDiOpenDeviceInterface function retrieves information about a device interface and adds the interface to the specified device information set for a local system or a remote system.
old-location: devinst\setupdiopendeviceinterface.htm
tech.root: devinst
ms.assetid: 31ce43e5-08b4-4c1d-b31f-77ee4e278927
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: SetupDiOpenDeviceInterface, SetupDiOpenDeviceInterface function [Device and Driver Installation], SetupDiOpenDeviceInterfaceA, SetupDiOpenDeviceInterfaceW, devinst.setupdiopendeviceinterface, di-rtns_4505f6a3-e634-4070-a9b3-1487c2808838.xml, setupapi/SetupDiOpenDeviceInterface
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Setupapi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiOpenDeviceInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiOpenDeviceInterfaceA function


## -description


The <b>SetupDiOpenDeviceInterface</b> function retrieves information about a device interface and adds the interface to the specified device information set for a local system or a remote system. 


## -parameters




### -param DeviceInfoSet [in]

A pointer to a <a href="https://msdn.microsoft.com/library/Ff541247(v=VS.85).aspx">device information set</a> that contains, or will contain, a device information element that represents the device that supports the interface to open.


### -param DevicePath [in]

A pointer to a NULL-terminated string that supplies the name of the device interface to be opened. This name is a Win32 device path that is typically received in a PnP notification structure or obtained by a previous call to <a href="https://msdn.microsoft.com/5095404d-2447-407e-99e2-dd3ef3c3b905">SetupDiEnumDeviceInterfaces</a> and its related functions.


### -param OpenFlags [in]

Flags that determine how the device interface element is to be opened. The only valid flag is as follows: 





#### DIODI_NO_ADD

Specifies that the device information element for the underlying device will not be created if that element is not already present in the specified <a href="https://msdn.microsoft.com/library/Ff541247(v=VS.85).aspx">device information set</a>. For more information, see the following <b>Remarks</b> section. 


### -param DeviceInterfaceData [out, optional]

A pointer to a caller-initialized  <a href="https://msdn.microsoft.com/df142e95-aa1c-4d3e-90c6-bac86effbd5d">SP_DEVICE_INTERFACE_DATA</a> structure that receives the requested interface data. This pointer is optional and can be <b>NULL</b>. If a buffer is supplied, the caller must set the <b>cbSize</b> member of the structure to <b>sizeof(</b>SP_DEVICE_INTERFACE_DATA<b>)</b> before calling <b>SetupDiOpenDeviceInterface</b>. For more information, see the following <b>Remarks</b> section.


## -returns



<b>SetupDiOpenDeviceInterface</b> returns <b>TRUE</b> if the function completed without error. If the function completed with an error, it returns <b>FALSE</b> and the error code for the failure can be retrieved by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



If a device interface element for the interface already exists in <i>DeviceInfoSet</i>, <b>SetupDiOpenDeviceInterface</b> updates the flags. Therefore, this function can be used to update the flags for a device interface. For example, an interface might have been inactive when it was first opened, but has subsequently become active. If the device information element for the underlying device is not already present in <i>DeviceInfoSet</i>, this function creates one and adds it to <i>DeviceInfoSet</i>. 

If the function successfully opens the new device interface but the caller did not supply a valid structure in the <i>DeviceInterfaceData</i> parameter, the function will return <b>FALSE</b> and a subsequent call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> will return ERROR_INVALID_USER_BUFFER. However, in this situation, <b>SetupDiOpenDeviceInterface</b> does add the requested interface to the device information set.

If the new device interface is successfully opened, but the caller-supplied <i>DeviceInterfaceData</i> buffer is invalid, this function returns <b>FALSE</b> and <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_INVALID_USER_BUFFER. The caller's buffer error does not prevent the interface from being opened.

If the DIODI_NO_ADD flag is specified for the <i>OpenFlags</i> parameter, and a device information element for the underlying device is not already present in the specified <a href="https://msdn.microsoft.com/library/Ff541247(v=VS.85).aspx">device information set</a>, this function returns <b>FALSE</b> and <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_NO_SUCH_DEVICE_INTERFACE. 

When the application has finished using the information that <b>SetupDiOpenDeviceInterface</b> retrieved<b>,</b> the application must call <a href="https://msdn.microsoft.com/20c9fe5b-ed88-4e2c-bca5-eba62f919fe6">SetupDiDeleteDeviceInterfaceData</a>.


<a href="https://msdn.microsoft.com/3d256dec-ec8c-4c62-883b-e2c292fd90eb">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK</a>attribute can be passed in as the value of the <i>DevicePath</i> argument of the <b>SetupDiOpenDeviceInterface</b> function.




## -see-also




<a href="https://msdn.microsoft.com/20c9fe5b-ed88-4e2c-bca5-eba62f919fe6">SetupDiDeleteDeviceInterfaceData</a>



<a href="https://msdn.microsoft.com/5095404d-2447-407e-99e2-dd3ef3c3b905">SetupDiEnumDeviceInterfaces</a>
 

 

