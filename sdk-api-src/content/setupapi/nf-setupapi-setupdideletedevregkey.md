---
UID: NF:setupapi.SetupDiDeleteDevRegKey
title: SetupDiDeleteDevRegKey function (setupapi.h)
description: The SetupDiDeleteDevRegKey function deletes specified user-accessible registry keys that are associated with a device information element.
helpviewer_keywords: ["SetupDiDeleteDevRegKey","SetupDiDeleteDevRegKey function [Device and Driver Installation]","devinst.setupdideletedevregkey","di-rtns_9e60aff0-2d01-4b1b-90e5-7f050a0e075a.xml","setupapi/SetupDiDeleteDevRegKey"]
old-location: devinst\setupdideletedevregkey.htm
tech.root: devinst
ms.assetid: 3b332291-0593-4750-9965-f6bf90ec8838
ms.date: 12/05/2018
ms.keywords: SetupDiDeleteDevRegKey, SetupDiDeleteDevRegKey function [Device and Driver Installation], devinst.setupdideletedevregkey, di-rtns_9e60aff0-2d01-4b1b-90e5-7f050a0e075a.xml, setupapi/SetupDiDeleteDevRegKey
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
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiDeleteDevRegKey
 - setupapi/SetupDiDeleteDevRegKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-setupapi-devobj-l1-1-0.dll
 - Setupapi.dll
api_name:
 - SetupDiDeleteDevRegKey
---

# SetupDiDeleteDevRegKey function


## -description

The <b>SetupDiDeleteDevRegKey</b> function deletes specified user-accessible registry keys that are associated with a device information element.

## -parameters

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains a device information element that represents the device for which to delete registry keys. The device information set must not contain remote elements.

### -param DeviceInfoData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.

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

Delete the device's <a href="/windows-hardware/drivers/">hardware key</a>.



#### DIREG_DRV

Delete the device's <a href="/windows-hardware/drivers/">software key</a>.



#### DIREG_BOTH

Delete both the hardware and software keys for the device.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The caller of this function must be a member of the Administrators group.

The <i>DeviceInfoSet</i> must only contain elements on the local computer.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedevregkeya">SetupDiCreateDevRegKey</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigethwprofilelist">SetupDiGetHwProfileList</a>