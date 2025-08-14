---
UID: NF:shellapi.NetAddr_DisplayErrorTip
title: NetAddr_DisplayErrorTip macro (shellapi.h)
description: Displays an error message in the balloon tip associated with the network address control.
helpviewer_keywords: ["NetAddr_DisplayErrorTip","NetAddr_DisplayErrorTip macro [Windows Shell]","_shell_NetAddr_DisplayErrorTip","shell.NetAddr_DisplayErrorTip","shellapi/NetAddr_DisplayErrorTip"]
old-location: shell\NetAddr_DisplayErrorTip.htm
tech.root: shell
ms.assetid: 1fd623da-51a0-4b37-a25b-00278b5f4732
ms.date: 07/01/2025
ms.keywords: NetAddr_DisplayErrorTip, NetAddr_DisplayErrorTip macro [Windows Shell], _shell_NetAddr_DisplayErrorTip, shell.NetAddr_DisplayErrorTip, shellapi/NetAddr_DisplayErrorTip
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetAddr_DisplayErrorTip
 - shellapi/NetAddr_DisplayErrorTip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shellapi.h
api_name:
 - NetAddr_DisplayErrorTip
---

# NetAddr_DisplayErrorTip macro

## -syntax

```cpp
HRESULT NetAddr_DisplayErrorTip(
  [in]  HWND hwnd
);
```

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**




## -description

Displays an error message in the balloon tip associated with the network address control.

## -parameters

### -param hwnd [in]

A handle to the network address control.

## -remarks

Call this macro to display an error message when an address typed into the control does not validate against the allowed network address types set with macro <a href="/windows/desktop/api/shellapi/nf-shellapi-netaddr_setallowtype">NetAddr_SetAllowType</a>. Use the macro <a href="/windows/desktop/api/shellapi/nf-shellapi-netaddr_getaddress">NetAddr_GetAddress</a> to validate the address.

## -see-also

<a href="/windows/desktop/api/shellapi/nf-shellapi-netaddr_getallowtype">NetAddr_GetAllowType</a>
