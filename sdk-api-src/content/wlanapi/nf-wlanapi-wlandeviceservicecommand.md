---
UID: NF:wlanapi.WlanDeviceServiceCommand
title: WlanDeviceServiceCommand
description: Allows an OEM or IHV component to communicate with a device service on a particular wireless LAN interface.
tech.root: nwifi
helpviewer_keywords: ["WlanDeviceServiceCommand"]
ms.date: 01/07/2019
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wlanapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: OneCoreUAP.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - wlanapi.dll
api_name:
 - WlanDeviceServiceCommand
f1_keywords:
 - WlanDeviceServiceCommand
 - wlanapi/WlanDeviceServiceCommand
dev_langs:
 - c++
---

## -description

Allows an original equipment manufacturer (OEM) or independent hardware vendor (IHV) component to communicate with a device service on a particular wireless LAN interface.

## -parameters

### -param hClientHandle [in]

Type: **[HANDLE](/windows/win32/winprog/windows-data-types)**

The client's session handle, obtained by a previous call to the [WlanOpenHandle](./nf-wlanapi-wlanopenhandle.md) function.

### -param pInterfaceGuid [in]

Type: **CONST [GUID](../guiddef/ns-guiddef-guid.md)\***

A pointer to the **GUID** of the wireless LAN interface to be queried. You can determine the **GUID** of each wireless LAN interface enabled on a local computer by using the [WlanEnumInterfaces](./nf-wlanapi-wlanenuminterfaces.md) function.

### -param pDeviceServiceGuid [in]

Type: **[GUID](../guiddef/ns-guiddef-guid.md)\***

The **GUID** identifying the device service for this command.

### -param dwOpCode [in]

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

The operational code identifying the operation to be performed on the device service.

### -param dwInBufferSize [in]

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

The size, in bytes, of the input buffer.

### -param pInBuffer [in]

Type: **[PVOID](/windows/win32/winprog/windows-data-types)**

A generic buffer for command input.

### -param dwOutBufferSize [in]

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

The size, in bytes, of the output buffer.

### -param pOutBuffer [in, out, optional]

Type: **[PVOID](/windows/win32/winprog/windows-data-types)**

A generic buffer for command output.

### -param pdwBytesReturned [out]

Type: **[PDWORD](/windows/win32/winprog/windows-data-types)**

The number of bytes returned.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, the return value is **ERROR_SUCCESS**. If the function fails with **ERROR_ACCESS_DENIED**, then the caller doesn't have sufficient permissions to perform this operation. The caller needs to either have admin privilege, or needs to be a UMDF driver.

## -remarks

## -see-also
