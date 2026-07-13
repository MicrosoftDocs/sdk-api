---
UID: NF:mdmregistration.SetDeviceManagementConfigInfo
title: SetDeviceManagementConfigInfo
description: Sets the config info associated with the provider ID.
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
 - SetDeviceManagementConfigInfo
f1_keywords:
 - SetDeviceManagementConfigInfo
 - mdmregistration/SetDeviceManagementConfigInfo
dev_langs:
 - c++
---

## -description

Sets the config info associated with the provider ID.

## -parameters

### -param providerID

Type: \_In\_ **[PCWSTR](/windows/win32/winprog/windows-data-types)**

A string containing the provider ID.

### -param configString

Type: \_In\_ **[PCWSTR](/windows/win32/winprog/windows-data-types)**

A string containing the config info (the data to write).

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -remarks

## -see-also
