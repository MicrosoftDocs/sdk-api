---
UID: NF:setupapi.SetupDiOpenClassRegKey
title: SetupDiOpenClassRegKey function (setupapi.h)
description: The SetupDiOpenClassRegKey function opens the setup class registry key or a specific class's subkey.
helpviewer_keywords: ["SetupDiOpenClassRegKey","SetupDiOpenClassRegKey function [Device and Driver Installation]","devinst.setupdiopenclassregkey","di-rtns_2bdb6a33-58be-4799-af21-40f807a9fab8.xml","setupapi/SetupDiOpenClassRegKey"]
old-location: devinst\setupdiopenclassregkey.htm
tech.root: devinst
ms.assetid: 22afdbd4-91fc-44c6-ad16-0c3c1adf8c70
ms.date: 12/05/2018
ms.keywords: SetupDiOpenClassRegKey, SetupDiOpenClassRegKey function [Device and Driver Installation], devinst.setupdiopenclassregkey, di-rtns_2bdb6a33-58be-4799-af21-40f807a9fab8.xml, setupapi/SetupDiOpenClassRegKey
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: DesktopFor universal, call CM_Open_Class_Key
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
 - SetupDiOpenClassRegKey
 - setupapi/SetupDiOpenClassRegKey
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
 - SetupDiOpenClassRegKey
---

# SetupDiOpenClassRegKey function


## -description

The <b>SetupDiOpenClassRegKey</b> function opens the setup class registry key or a specific class's subkey.

## -parameters

### -param ClassGuid [in, optional]

A pointer to the GUID of the setup class whose key is to be opened. This parameter is optional and can be <b>NULL</b>. If this parameter is <b>NULL</b>, the root of the setup class tree (<b>HKLM\SYSTEM\CurrentControlSet\Control\Class</b>) is opened.

### -param samDesired [in]

The registry security access for the key to be opened. For information about registry security access values of type REGSAM, see the Microsoft Windows SDK documentation.

## -returns

If the function is successful, it returns a handle to an opened registry key where information about this setup class can be stored/retrieved. 

If the function fails, it returns INVALID_HANDLE_VALUE. To get extended error information, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Depending on the value that is passed in the <i>samDesired</i> parameter, it might be necessary for the caller of this function to be a member of the Administrators group.

This function does not create a registry key if it does not already exist.

The handle returned from this function must be closed by calling <a href="/windows/win32/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>.

To open the interface class registry key or a specific interface class subkey, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopenclassregkeyexa">SetupDiOpenClassRegKeyEx</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopenclassregkeyexa">SetupDiOpenClassRegKeyEx</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopendevregkey">SetupDiOpenDevRegKey</a>