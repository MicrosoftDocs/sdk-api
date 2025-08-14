---
UID: NF:setupapi.SetupDiGetDeviceInfoListDetailA
title: SetupDiGetDeviceInfoListDetailA function (setupapi.h)
description: The SetupDiGetDeviceInfoListDetail function retrieves information associated with a device information set including the class GUID, remote computer handle, and remote computer name. (ANSI)
helpviewer_keywords: ["SetupDiGetDeviceInfoListDetailA", "di-rtns_b25a6105-3c1f-4b79-ad07-37be79fa36ae.xml"]
old-location: devinst\setupdigetdeviceinfolistdetail.htm
tech.root: devinst
ms.assetid: 3f624882-9ccc-4be1-92aa-8bba9f0022ea
ms.date: 12/05/2018
ms.keywords: SetupDiGetDeviceInfoListDetail, SetupDiGetDeviceInfoListDetail function [Device and Driver Installation], SetupDiGetDeviceInfoListDetailA, SetupDiGetDeviceInfoListDetailW, devinst.setupdigetdeviceinfolistdetail, di-rtns_b25a6105-3c1f-4b79-ad07-37be79fa36ae.xml, setupapi/SetupDiGetDeviceInfoListDetail
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiGetDeviceInfoListDetailA
 - setupapi/SetupDiGetDeviceInfoListDetailA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - ext-ms-win-setupapi-devobj-l1-1-0.dll
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiGetDeviceInfoListDetail - SetupDiGetDeviceInfoListDetailA
---

# SetupDiGetDeviceInfoListDetailA function


## -description

The <b>SetupDiGetDeviceInfoListDetail</b> function retrieves information associated with a device information set including the class GUID, remote computer handle, and remote computer name.

## -parameters

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> for which to retrieve information.

### -param DeviceInfoSetDetailData [out]

A pointer to a caller-initialized <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_list_detail_data_a">SP_DEVINFO_LIST_DETAIL_DATA</a> structure that receives the device information set information. For more information about this structure, see the following <b>Remarks</b> section.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the parameters are valid, <b>SetupDiGetDeviceInfoListDetail</b> sets values in the <i>DeviceInfoSetDetailData</i> structure (except for the <b>cbSize</b> field) and returns status NO_ERROR. 

A caller of <b>SetupDiGetDeviceInfoListDetail</b> must set <i>DeviceInfoSetDetailData.</i><b>cbSize</b> to <b>sizeof</b>(SP_DEVINFO_LIST_DETAIL_DATA) or the function will fail and the call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return ERROR_INVALID_USER_BUFFER.

If <b>SetupDiGetDeviceInfoListDetail</b> completes successfully, <i>DeviceInfoSetDetailData.</i><b>ClassGuid</b> contains the class GUID associated with the device information set or a GUID_NULL structure.

If <b>SetupDiGetDeviceInfoListDetail</b> completes successfully and the device information set is for a remote system, <i>DeviceInfoSetDetailData.</i><b>RemoteMachineHandle</b> contains the ConfigMgr32 system handle for accessing the remote system and <i>DeviceInfoSetDetailData.</i><b>RemoteMachineName</b> contains the name of the remote system. If there is a remote handle for the device information set, it must be used when calling <b>CM_</b><i>Xxx</i><b>_Ex</b> functions because the DevInst handles are relative to the remote handle.

If the device information set is for the local computer, <i>DeviceInfoSetDetailData.</i><b>RemoteMachineHandle</b> is <b>NULL</b> and <i>DeviceInfoSetDetailData.</i><b>RemoteMachineName</b> is an empty string. 





> [!NOTE]
> The setupapi.h header defines SetupDiGetDeviceInfoListDetail as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinfolistexa">SetupDiCreateDeviceInfoListEx</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsexa">SetupDiGetClassDevsEx</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinfolistclass">SetupDiGetDeviceInfoListClass</a>
