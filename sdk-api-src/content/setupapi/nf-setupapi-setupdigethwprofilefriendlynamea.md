---
UID: NF:setupapi.SetupDiGetHwProfileFriendlyNameA
title: SetupDiGetHwProfileFriendlyNameA function (setupapi.h)
description: The SetupDiGetHwProfileFriendlyName function retrieves the friendly name associated with a hardware profile ID. (ANSI)
helpviewer_keywords: ["SetupDiGetHwProfileFriendlyNameA", "di-rtns_3a055603-6e43-449a-bfd0-fbd7434bebfe.xml"]
old-location: devinst\setupdigethwprofilefriendlyname.htm
tech.root: devinst
ms.assetid: 92f08c8a-b31a-4f88-8ff5-c60d985b79bf
ms.date: 12/05/2018
ms.keywords: SetupDiGetHwProfileFriendlyName, SetupDiGetHwProfileFriendlyName function [Device and Driver Installation], SetupDiGetHwProfileFriendlyNameA, SetupDiGetHwProfileFriendlyNameW, devinst.setupdigethwprofilefriendlyname, di-rtns_3a055603-6e43-449a-bfd0-fbd7434bebfe.xml, setupapi/SetupDiGetHwProfileFriendlyName
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
 - SetupDiGetHwProfileFriendlyNameA
 - setupapi/SetupDiGetHwProfileFriendlyNameA
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
 - SetupDiGetHwProfileFriendlyName
 - SetupDiGetHwProfileFriendlyNameA
---

# SetupDiGetHwProfileFriendlyNameA function


## -description

The <b>SetupDiGetHwProfileFriendlyName</b> function retrieves the friendly name associated with a hardware profile ID.

## -parameters

### -param HwProfile [in]

The hardware profile ID associated with the friendly name to retrieve. If this parameter is 0, the friendly name for the current hardware profile is retrieved.

### -param FriendlyName [out]

A pointer to a string buffer to receive the friendly name.

### -param FriendlyNameSize [in]

The size, in characters, of the <i>FriendlyName</i> buffer.

### -param RequiredSize [out, optional]

A pointer to a variable of type DWORD that receives the number of characters required to retrieve the friendly name (including a NULL terminator).

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigethwprofilefriendlynameexa">SetupDiGetHwProfileFriendlyNameEx</a> to get the friendly name of a hardware profile ID on a remote computer.





> [!NOTE]
> The setupapi.h header defines SetupDiGetHwProfileFriendlyName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigethwprofilefriendlynameexa">SetupDiGetHwProfileFriendlyNameEx</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigethwprofilelist">SetupDiGetHwProfileList</a>
