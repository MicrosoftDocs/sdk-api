---
UID: NF:setupapi.SetupDiClassGuidsFromNameExW
title: SetupDiClassGuidsFromNameExW function (setupapi.h)
description: The SetupDiClassGuidsFromNameEx function retrieves the GUIDs associated with the specified class name. This resulting list contains the classes currently installed on a local or remote computer. (Unicode)
helpviewer_keywords: ["SetupDiClassGuidsFromNameEx", "SetupDiClassGuidsFromNameEx function [Device and Driver Installation]", "SetupDiClassGuidsFromNameExW", "devinst.setupdiclassguidsfromnameex", "di-rtns_de553347-9025-4477-8d83-9d1bdac1ceff.xml", "setupapi/SetupDiClassGuidsFromNameEx"]
old-location: devinst\setupdiclassguidsfromnameex.htm
tech.root: devinst
ms.assetid: 5a692ed0-2e3a-464e-934e-2fe98d9c217b
ms.date: 01/30/2023
ms.keywords: SetupDiClassGuidsFromNameEx, SetupDiClassGuidsFromNameEx function [Device and Driver Installation], SetupDiClassGuidsFromNameExA, SetupDiClassGuidsFromNameExW, devinst.setupdiclassguidsfromnameex, di-rtns_de553347-9025-4477-8d83-9d1bdac1ceff.xml, setupapi/SetupDiClassGuidsFromNameEx
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
 - SetupDiClassGuidsFromNameExW
 - setupapi/SetupDiClassGuidsFromNameExW
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
 - SetupDiClassGuidsFromNameEx
 - SetupDiClassGuidsFromNameExW
---

# SetupDiClassGuidsFromNameExW function


## -description

The <b>SetupDiClassGuidsFromNameEx</b> function retrieves the GUIDs associated with the specified class name. This resulting list contains the classes currently installed on a local or remote computer.

## -parameters

### -param ClassName [in]

The name of the class for which to retrieve the class GUIDs.

### -param ClassGuidList [out]

A pointer to an array to receive the list of GUIDs associated with the specified class name.

### -param ClassGuidListSize [in]

The number of GUIDs in the <i>ClassGuidList</i> array.

### -param RequiredSize [out]

A pointer to a variable that receives the number of GUIDs associated with the class name. If this number is greater than the size of the <i>ClassGuidList</i> buffer, the number indicates how large the array must be in order to store all the GUIDs.

### -param MachineName [in, optional]

A pointer to a NULL-terminated string that contains the name of a remote system from which to retrieve the GUIDs. This parameter is optional and can be <b>NULL</b>. If <i>MachineName</i> is <b>NULL</b>, the local system name is used.

> [!CAUTION]
> Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.

### -param Reserved

Must be <b>NULL</b>.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Class names are not guaranteed to be unique; only GUIDs are unique. Therefore, one class name can return more than one GUID.





> [!NOTE]
> The setupapi.h header defines SetupDiClassGuidsFromNameEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiclassguidsfromnamea">SetupDiClassGuidsFromName</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiclassnamefromguidexa">SetupDiClassNameFromGuidEx</a>
