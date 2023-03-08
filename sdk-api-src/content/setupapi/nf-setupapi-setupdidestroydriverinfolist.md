---
UID: NF:setupapi.SetupDiDestroyDriverInfoList
title: SetupDiDestroyDriverInfoList function (setupapi.h)
description: The SetupDiDestroyDriverInfoList function deletes a driver list.
helpviewer_keywords: ["SetupDiDestroyDriverInfoList","SetupDiDestroyDriverInfoList function [Device and Driver Installation]","devinst.setupdidestroydriverinfolist","di-rtns_6eade614-a4f8-40cc-beb7-0d6728b1ad53.xml","setupapi/SetupDiDestroyDriverInfoList"]
old-location: devinst\setupdidestroydriverinfolist.htm
tech.root: devinst
ms.assetid: d8067609-1046-4641-9f57-b0ee2be5a3b2
ms.date: 12/05/2018
ms.keywords: SetupDiDestroyDriverInfoList, SetupDiDestroyDriverInfoList function [Device and Driver Installation], devinst.setupdidestroydriverinfolist, di-rtns_6eade614-a4f8-40cc-beb7-0d6728b1ad53.xml, setupapi/SetupDiDestroyDriverInfoList
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
 - SetupDiDestroyDriverInfoList
 - setupapi/SetupDiDestroyDriverInfoList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupDiDestroyDriverInfoList
req.apiset: ext-ms-win-setupapi-classinstallers-l1-1-2 (introduced in Windows 10, version 10.0.14393)
---

# SetupDiDestroyDriverInfoList function


## -description

The <b>SetupDiDestroyDriverInfoList</b> function deletes a driver list.

## -parameters

### -param DeviceInfoSet [in]

A handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains the driver list to delete.

### -param DeviceInfoData [in, optional]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be set to <b>NULL</b>. If this parameter is specified, <b>SetupDiDestroyDriverInfoList</b> deletes the driver list for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiDestroyDriverInfoList</b> deletes the global class driver list that is associated with <i>DeviceInfoSet</i>.

### -param DriverType [in]

The type of driver list to delete, which must be one of the following values:





#### SPDIT_CLASSDRIVER

Delete a list of class drivers. If <i>DeviceInfoData</i> is <b>NULL</b>, this driver list type must be specified.



#### SPDIT_COMPATDRIVER

Delete a list of compatible drivers for the specified device. <i>DeviceInfoData</i> must be specified if this driver list type is specified.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the currently selected driver is a member of the list being deleted, the selection is reset.

If a class driver list is being deleted, the DI_FLAGSEX_DIDINFOLIST and DI_DIDCLASS flags are reset for the corresponding device information set or device information element. The DI_MULTMFGS flags is also reset.

If a compatible driver list is being destroyed, the DI_FLAGSEX_DIDCOMPATINFO and DI_DIDCOMPAT flags are reset for the corresponding device information element.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuilddriverinfolist">SetupDiBuildDriverInfoList</a>
