---
UID: NF:setupapi.SetupDiClassNameFromGuidExA
title: SetupDiClassNameFromGuidExA function (setupapi.h)
description: The SetupDiClassNameFromGuidEx function retrieves the class name associated with a class GUID. The class can be installed on a local or remote computer. (ANSI)
helpviewer_keywords: ["SetupDiClassNameFromGuidExA", "di-rtns_69da61fd-b042-4b1b-92a4-d40418f18794.xml"]
old-location: devinst\setupdiclassnamefromguidex.htm
tech.root: devinst
ms.assetid: 0d576df1-e259-4025-8ef0-a520f5680fa0
ms.date: 01/30/2023
ms.keywords: SetupDiClassNameFromGuidEx, SetupDiClassNameFromGuidEx function [Device and Driver Installation], SetupDiClassNameFromGuidExA, SetupDiClassNameFromGuidExW, devinst.setupdiclassnamefromguidex, di-rtns_69da61fd-b042-4b1b-92a4-d40418f18794.xml, setupapi/SetupDiClassNameFromGuidEx
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
 - SetupDiClassNameFromGuidExA
 - setupapi/SetupDiClassNameFromGuidExA
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
 - SetupDiClassNameFromGuidEx
 - SetupDiClassNameFromGuidExA
---

# SetupDiClassNameFromGuidExA function


## -description

The <b>SetupDiClassNameFromGuidEx</b> function retrieves the class name associated with a class GUID. The class can be installed on a local or remote computer.

## -parameters

### -param ClassGuid [in]

The class GUID of the class name to retrieve.

### -param ClassName [out]

A pointer to a string buffer that receives the NULL-terminated name of the class for the specified GUID.

### -param ClassNameSize [in]

The size, in characters, of the <i>ClassName</i> buffer.

### -param RequiredSize [out, optional]

The number of characters required to store the class name (including a terminating null). <i>RequiredSize</i> is always less than MAX_CLASS_NAME_LEN.

### -param MachineName [in, optional]

A pointer to a NULL-terminated string that contains the name of a remote system on which the class is installed. This parameter is optional and can be <b>NULL</b>. If <i>MachineName</i> is <b>NULL</b>, the local system name is used.

> [!CAUTION]
> Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.

### -param Reserved

Must be <b>NULL</b>.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiclassguidsfromnameexa">SetupDiClassGuidsFromNameEx</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiclassnamefromguida">SetupDiClassNameFromGuid</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupDiClassNameFromGuidEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
