---
UID: NF:setupapi.SetupDiGetDeviceInfoListClass
title: SetupDiGetDeviceInfoListClass function (setupapi.h)
description: The SetupDiGetDeviceInfoListClass function retrieves the GUID for the device setup class associated with a device information set if the set has an associated class.
helpviewer_keywords: ["SetupDiGetDeviceInfoListClass","SetupDiGetDeviceInfoListClass function [Device and Driver Installation]","devinst.setupdigetdeviceinfolistclass","di-rtns_219b6225-e6f3-40b4-8127-709c425a0cad.xml","setupapi/SetupDiGetDeviceInfoListClass"]
old-location: devinst\setupdigetdeviceinfolistclass.htm
tech.root: devinst
ms.assetid: 332945dc-9edc-4fbf-a4fa-533a00352553
ms.date: 12/05/2018
ms.keywords: SetupDiGetDeviceInfoListClass, SetupDiGetDeviceInfoListClass function [Device and Driver Installation], devinst.setupdigetdeviceinfolistclass, di-rtns_219b6225-e6f3-40b4-8127-709c425a0cad.xml, setupapi/SetupDiGetDeviceInfoListClass
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
 - SetupDiGetDeviceInfoListClass
 - setupapi/SetupDiGetDeviceInfoListClass
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
 - SetupDiGetDeviceInfoListClass
---

# SetupDiGetDeviceInfoListClass function


## -description

The <b>SetupDiGetDeviceInfoListClass</b> function retrieves the GUID for the <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a> associated with a device information set if the set has an associated class.

## -parameters

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> to query.

### -param ClassGuid [out]

A pointer to variable of type GUID that receives the GUID for the associated class.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the specified device information set does not have an associated class because a class GUID was not specified when the set was created with <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinfolist">SetupDiCreateDeviceInfoList</a>, the function fails. In this case, a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_NO_ASSOCIATED_CLASS.

If a device information set is for a remote computer, use <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinfolistdetaila">SetupDiGetDeviceInfoListDetail</a> to get the associated remote computer handle and computer name.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinfolist">SetupDiCreateDeviceInfoList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevs</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinfolistdetaila">SetupDiGetDeviceInfoListDetail</a>