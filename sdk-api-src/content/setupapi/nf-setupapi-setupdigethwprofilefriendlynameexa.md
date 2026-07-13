---
UID: NF:setupapi.SetupDiGetHwProfileFriendlyNameExA
title: SetupDiGetHwProfileFriendlyNameExA function (setupapi.h)
description: The SetupDiGetHwProfileFriendlyNameEx function retrieves the friendly name associated with a hardware profile ID on a local or remote computer. (ANSI)
helpviewer_keywords: ["SetupDiGetHwProfileFriendlyNameExA", "di-rtns_43d54c1e-047c-491c-93a1-cd5eff918a58.xml"]
old-location: devinst\setupdigethwprofilefriendlynameex.htm
tech.root: devinst
ms.assetid: 839c1e4c-cfa6-4f59-979c-24623a040d5c
ms.date: 01/30/2023
ms.keywords: SetupDiGetHwProfileFriendlyNameEx, SetupDiGetHwProfileFriendlyNameEx function [Device and Driver Installation], SetupDiGetHwProfileFriendlyNameExA, SetupDiGetHwProfileFriendlyNameExW, devinst.setupdigethwprofilefriendlynameex, di-rtns_43d54c1e-047c-491c-93a1-cd5eff918a58.xml, setupapi/SetupDiGetHwProfileFriendlyNameEx
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
 - SetupDiGetHwProfileFriendlyNameExA
 - setupapi/SetupDiGetHwProfileFriendlyNameExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiGetHwProfileFriendlyNameEx
 - SetupDiGetHwProfileFriendlyNameExA
---

# SetupDiGetHwProfileFriendlyNameExA function


## -description

The <b>SetupDiGetHwProfileFriendlyNameEx</b> function retrieves the friendly name associated with a hardware profile ID on a local or remote computer.

## -parameters

### -param HwProfile [in]

Supplies the hardware profile ID associated with the friendly name to retrieve. If this parameter is 0, the friendly name for the current hardware profile is retrieved.

### -param FriendlyName [out]

A pointer to a character buffer to receive the friendly name.

### -param FriendlyNameSize [in]

The size, in characters, of the <i>FriendlyName</i> buffer.

### -param RequiredSize [out, optional]

A pointer to a variable to receive the number of characters required to store the friendly name (including a NULL terminator). This parameter is optional and can be <b>NULL</b>.

### -param MachineName [in, optional]

A pointer to NULL-terminated string that contains the name of a remote computer on which the hardware profile ID resides. This parameter is optional and can be <b>NULL</b>. If <i>MachineName</i> is <b>NULL</b>, the hardware profile ID is on the local computer.

> [!CAUTION]
> Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.

### -param Reserved

Must be <b>NULL</b>.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigethwprofilefriendlynamea">SetupDiGetHwProfileFriendlyName</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigethwprofilelistexa">SetupDiGetHwProfileListEx</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupDiGetHwProfileFriendlyNameEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
