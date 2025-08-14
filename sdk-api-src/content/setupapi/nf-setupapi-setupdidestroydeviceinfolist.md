---
UID: NF:setupapi.SetupDiDestroyDeviceInfoList
title: SetupDiDestroyDeviceInfoList function (setupapi.h)
description: The SetupDiDestroyDeviceInfoList function deletes a device information set and frees all associated memory.
helpviewer_keywords: ["SetupDiDestroyDeviceInfoList","SetupDiDestroyDeviceInfoList function [Device and Driver Installation]","devinst.setupdidestroydeviceinfolist","di-rtns_f8a4a633-46fd-4d3f-81dc-68920ccebfd9.xml","setupapi/SetupDiDestroyDeviceInfoList"]
old-location: devinst\setupdidestroydeviceinfolist.htm
tech.root: devinst
ms.assetid: a341db0c-9ece-4677-9854-8e0dc29966c6
ms.date: 12/05/2018
ms.keywords: SetupDiDestroyDeviceInfoList, SetupDiDestroyDeviceInfoList function [Device and Driver Installation], devinst.setupdidestroydeviceinfolist, di-rtns_f8a4a633-46fd-4d3f-81dc-68920ccebfd9.xml, setupapi/SetupDiDestroyDeviceInfoList
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
 - SetupDiDestroyDeviceInfoList
 - setupapi/SetupDiDestroyDeviceInfoList
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
 - Ext-MS-Win-SetupAPI-ClassInstallers-l1-1-0.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-l1-1-1.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupDiDestroyDeviceInfoList
req.apiset: ext-ms-win-setupapi-classinstallers-l1-1-0 (introduced in Windows 8)
---

# SetupDiDestroyDeviceInfoList function


## -description

The <b>SetupDiDestroyDeviceInfoList</b> function deletes a device information set and frees all associated memory.

## -parameters

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> to delete.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinfolist">SetupDiCreateDeviceInfoList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevs</a>
