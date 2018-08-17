---
UID: NF:setupapi.SetupDiDeleteDevRegKey
title: SetupDiDeleteDevRegKey function
author: windows-sdk-content
description: The SetupDiDeleteDevRegKey function deletes specified user-accessible registry keys that are associated with a device information element.
old-location: devinst\setupdideletedevregkey.htm
old-project: devinst
ms.assetid: 3b332291-0593-4750-9965-f6bf90ec8838
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetupDiDeleteDevRegKey, SetupDiDeleteDevRegKey function [Device and Driver Installation], devinst.setupdideletedevregkey, di-rtns_9e60aff0-2d01-4b1b-90e5-7f050a0e075a.xml, setupapi/SetupDiDeleteDevRegKey
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
 - SetupDiDeleteDevRegKey
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupDiDeleteDevRegKey function


## -description


The <b>SetupDiDeleteDevRegKey</b> function deletes specified user-accessible registry keys that are associated with a device information element.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> that contains a device information element that represents the device for which to delete registry keys. The device information set must not contain remote elements.


### -param DeviceInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.


### -param Scope [in]

The scope of the registry key to delete. The scope indicates where the information is located. The key can be global or hardware profile-specific. Can be one of the following values:





#### DICS_FLAG_GLOBAL

Delete the key that stores global configuration information. 



#### DICS_FLAG_CONFIGSPECIFIC

Delete the key that stores hardware profile-specific configuration information. 


### -param HwProfile [in]

If <i>Scope</i> is set to DICS_FLAG_CONFIGSPECIFIC, the <i>HwProfile</i> parameter specifies the hardware profile for which to delete the registry key. If <i>HwProfile</i> is 0, the key for the current hardware profile is deleted. If <i>HwProfile</i> is 0xFFFFFFFF, the registry key for all hardware profiles is deleted. 


### -param KeyType [in]

The type of registry storage key to delete. Can be one of the following values:





#### DIREG_DEV

Delete the device's <a href="https://msdn.microsoft.com/3be5c842-d1b6-4c34-8990-e23e2d08dd23">hardware key</a>.



#### DIREG_DRV

Delete the device's <a href="https://msdn.microsoft.com/5f6fec1a-1134-4765-81be-9b50939e5e66">software key</a>.



#### DIREG_BOTH

Delete both the hardware and software keys for the device.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



The caller of this function must be a member of the Administrators group.

The <i>DeviceInfoSet</i> must only contain elements on the local computer.




## -see-also




<a href="https://msdn.microsoft.com/8c07db95-eb59-4e01-851d-f6a8da169625">SetupDiCreateDevRegKey</a>



<a href="https://msdn.microsoft.com/59fc7202-0e03-4eaa-b3ca-7d55be767b1a">SetupDiGetHwProfileList</a>
 

 

