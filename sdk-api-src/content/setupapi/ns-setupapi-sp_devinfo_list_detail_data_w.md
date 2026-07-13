---
UID: NS:setupapi._SP_DEVINFO_LIST_DETAIL_DATA_W
title: SP_DEVINFO_LIST_DETAIL_DATA_W (setupapi.h)
description: An SP_DEVINFO_LIST_DETAIL_DATA structure contains information about a device information set, such as its associated setup class GUID (if it has an associated setup class). (Unicode)
helpviewer_keywords: ["*PSP_DEVINFO_LIST_DETAIL_DATA_W","PSP_DEVINFO_LIST_DETAIL_DATA","PSP_DEVINFO_LIST_DETAIL_DATA structure pointer [Device and Driver Installation]","SP_DEVINFO_LIST_DETAIL_DATA","SP_DEVINFO_LIST_DETAIL_DATA structure [Device and Driver Installation]","SP_DEVINFO_LIST_DETAIL_DATA_W","devinst.sp_devinfo_list_detail_data","di-struct_8539bcfc-25ee-49f5-bc59-74efc6aae5bf.xml","setupapi/PSP_DEVINFO_LIST_DETAIL_DATA","setupapi/SP_DEVINFO_LIST_DETAIL_DATA"]
old-location: devinst\sp_devinfo_list_detail_data.htm
tech.root: devinst
ms.assetid: 03e6c137-5a7f-443d-878f-5e5c6642dde9
ms.date: 12/05/2018
ms.keywords: '*PSP_DEVINFO_LIST_DETAIL_DATA_W, PSP_DEVINFO_LIST_DETAIL_DATA, PSP_DEVINFO_LIST_DETAIL_DATA structure pointer [Device and Driver Installation], SP_DEVINFO_LIST_DETAIL_DATA, SP_DEVINFO_LIST_DETAIL_DATA structure [Device and Driver Installation], SP_DEVINFO_LIST_DETAIL_DATA_W, devinst.sp_devinfo_list_detail_data, di-struct_8539bcfc-25ee-49f5-bc59-74efc6aae5bf.xml, setupapi/PSP_DEVINFO_LIST_DETAIL_DATA, setupapi/SP_DEVINFO_LIST_DETAIL_DATA'
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SP_DEVINFO_LIST_DETAIL_DATA_W, *PSP_DEVINFO_LIST_DETAIL_DATA_W
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_DEVINFO_LIST_DETAIL_DATA_W
 - setupapi/_SP_DEVINFO_LIST_DETAIL_DATA_W
 - PSP_DEVINFO_LIST_DETAIL_DATA_W
 - setupapi/PSP_DEVINFO_LIST_DETAIL_DATA_W
 - SP_DEVINFO_LIST_DETAIL_DATA_W
 - setupapi/SP_DEVINFO_LIST_DETAIL_DATA_W
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - setupapi.h
api_name:
 - SP_DEVINFO_LIST_DETAIL_DATA
 - sp_devinfo_list_detail_data_w
---

# SP_DEVINFO_LIST_DETAIL_DATA_W structure


## -description

An SP_DEVINFO_LIST_DETAIL_DATA structure contains information about a device information set, such as its associated setup class GUID (if it has an associated setup class).

## -struct-fields

### -field cbSize

The size, in bytes, of the SP_DEVINFO_LIST_DETAIL_DATA structure.

### -field ClassGuid

The setup class GUID that is associated with the device information set or GUID_NULL if there is no associated setup class.

### -field RemoteMachineHandle

If the device information set is for a remote computer, this member is a configuration manager machine handle for the remote computer. If the device information set is for the local computer, this member is <b>NULL</b>. 

This is typically the parameter that components use to access the remote computer. The <b>RemoteMachineName</b> contains a string, in case the component requires the name of the remote computer.

### -field RemoteMachineName

A NULL-terminated string that contains the name of the remote computer. If the device information set is for the local computer, this member is an empty string.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinfolistdetaila">SetupDiGetDeviceInfoListDetail</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SP_DEVINFO_LIST_DETAIL_DATA as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
