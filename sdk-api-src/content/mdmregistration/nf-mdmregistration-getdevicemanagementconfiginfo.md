---
UID: NF:mdmregistration.GetDeviceManagementConfigInfo
title: GetDeviceManagementConfigInfo
description: Gets the config info associated with the provider ID.
ms.date: 11/19/2020
tech.root: MDMReg
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: MDMRegistration.dll
req.header: mdmregistration.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: MDMRegistration.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - MDMRegistration.dll
api_name:
 - GetDeviceManagementConfigInfo
f1_keywords:
 - GetDeviceManagementConfigInfo
 - mdmregistration/GetDeviceManagementConfigInfo
dev_langs:
 - c++
---

## -description

Gets the config info associated with the provider ID.

## -parameters

### -param providerID

Type: \_In\_ **[PCWSTR](/windows/win32/winprog/windows-data-types)**

A string containing the provider ID.

### -param configStringBufferLength

Type: \_Inout\_ **[DWORD](/windows/win32/winprog/windows-data-types)\***

A pointer to the buffer length (the size of *configString* in chars).

### -param configString

Type: \_Out\_writes\_to\_opt\_(*configStringBufferLength, *configStringBufferLength) **[PWSTR](/windows/win32/winprog/windows-data-types)**

A buffer which, if the function completes successfully, will contain the config info.

If the buffer isn't large enough to hold the data, then the function returns **ERROR_MORE_DATA**, and stores the required buffer size in the variable pointed to by *configStringBufferLength*. In that case, the contents of the *configString* buffer are undefined.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -remarks

## -see-also
