---
UID: NF:setupapi.SetupDiGetHwProfileListExW
title: SetupDiGetHwProfileListExW function (setupapi.h)
description: The SetupDiGetHwProfileListEx function retrieves a list of all currently defined hardware profile IDs on a local or remote computer. (Unicode)
helpviewer_keywords: ["SetupDiGetHwProfileListEx", "SetupDiGetHwProfileListEx function [Device and Driver Installation]", "SetupDiGetHwProfileListExW", "devinst.setupdigethwprofilelistex", "di-rtns_ef3bbf07-27d9-48fc-86a2-1bdfc10cbc33.xml", "setupapi/SetupDiGetHwProfileListEx"]
old-location: devinst\setupdigethwprofilelistex.htm
tech.root: devinst
ms.assetid: add700ee-48aa-47dd-8b55-6338dea05bfb
ms.date: 01/30/2023
ms.keywords: SetupDiGetHwProfileListEx, SetupDiGetHwProfileListEx function [Device and Driver Installation], SetupDiGetHwProfileListExA, SetupDiGetHwProfileListExW, devinst.setupdigethwprofilelistex, di-rtns_ef3bbf07-27d9-48fc-86a2-1bdfc10cbc33.xml, setupapi/SetupDiGetHwProfileListEx
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
 - SetupDiGetHwProfileListExW
 - setupapi/SetupDiGetHwProfileListExW
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
 - SetupDiGetHwProfileListEx
 - SetupDiGetHwProfileListExW
---

# SetupDiGetHwProfileListExW function


## -description

The <b>SetupDiGetHwProfileListEx</b> function retrieves a list of all currently defined hardware profile IDs on a local or remote computer.

## -parameters

### -param HwProfileList [out]

A pointer to an array to receive the list of currently defined hardware profile IDs.

### -param HwProfileListSize [in]

The number of DWORDs in the <i>HwProfileList</i> buffer.

### -param RequiredSize [out]

A pointer to a variable of type DWORD that receives the number of hardware profiles that are currently defined. If the number is larger than <i>HwProfileListSize</i>, the list is truncated to fit the array size. The value returned in <i>RequiredSize</i> indicates the array size required to store the entire list of hardware profiles.

### -param CurrentlyActiveIndex [out, optional]

A pointer to a variable that receives the index of the currently active hardware profile in the retrieved hardware profile list. This parameter is optional and can be <b>NULL</b>.

### -param MachineName [in, optional]

A pointer to a NULL-terminated string that contains the name of a remote system for which to retrieve the list of hardware profile IDs. This parameter is optional and can be <b>NULL</b>. If this parameter is <b>NULL</b>, the list is retrieved for the local system.

> [!CAUTION]
> Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.

### -param Reserved

Must be <b>NULL</b>.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the required size is larger than <i>HwProfileListSize</i>, <b>SetupDiGetHwProfileListEx</b> returns <b>FALSE</b> and a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigethwprofilefriendlynameexa">SetupDiGetHwProfileFriendlyNameEx</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupDiGetHwProfileListEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
