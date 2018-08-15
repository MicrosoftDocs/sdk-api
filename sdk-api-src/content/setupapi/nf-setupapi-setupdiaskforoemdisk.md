---
UID: NF:setupapi.SetupDiAskForOEMDisk
title: SetupDiAskForOEMDisk function
author: windows-sdk-content
description: The SetupDiAskForOEMDisk function displays a dialog that asks the user for the path of an OEM installation disk.
old-location: devinst\setupdiaskforoemdisk.htm
old-project: devinst
ms.assetid: 5be03143-3de0-43ed-a027-832f1e275527
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetupDiAskForOEMDisk, SetupDiAskForOEMDisk function [Device and Driver Installation], devinst.setupdiaskforoemdisk, di-rtns_4b903984-cb48-48d3-9de8-dc68a79128c2.xml, setupapi/SetupDiAskForOEMDisk
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.redist: 
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
 - SetupDiAskForOEMDisk
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupDiAskForOEMDisk function


## -description


The <b>SetupDiAskForOEMDisk</b> function displays a dialog that asks the user for the path of an OEM installation disk.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="https://msdn.microsoft.com/library/Ff541247(v=VS.85).aspx">device information set</a> for the local computer. This set contains a device information element that represents the device that is being installed. 


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiAskForOEMDisk</b> associates the driver with the device that is being installed. If this parameter is <b>NULL</b>, <b>SetupDiAskForOEMDisk</b> associates the driver with the global class driver list for <i>DeviceInfoSet</i>.


## -returns



The function returns <b>TRUE</b> if it is successful and the <b>DriverPath</b> field of the SP_DEVINSTALLPARAMS structure is updated to reflect the new path. If the user cancels the dialog, the function returns <b>FALSE</b> and a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_CANCELLED.




## -remarks



<b>SetupDiAskForOEMDisk</b> allows the user to browse local and network drives for OEM installation files. However, <b>SetupDiAskForOEMDisk</b> is primarily designed to obtain the path of an OEM driver on a local computer before selecting and installing the driver for a device on that computer.

Although this function will not fail if the device information set if for a remote computer, the result is of limited use because the device information set cannot subsequently be used with DIF_<i>Xxx</i> installation requests or <b>SetupDi</b><i>Xxx</i> functions that do not support operations on a remote computer.

In particular, the device information set cannot be used as input with a DIF_SELECTDEVICE installation request to select a driver for a device, followed by a DIF_INSTALLDEVICE installation request to install a device on a remote computer.




## -see-also




<a href="https://msdn.microsoft.com/e97f0569-419a-4a9a-a657-fd972b160269">SetupDiSelectOEMDrv</a>
 

 

