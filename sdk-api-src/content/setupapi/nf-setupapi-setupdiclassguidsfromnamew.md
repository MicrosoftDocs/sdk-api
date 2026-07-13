---
UID: NF:setupapi.SetupDiClassGuidsFromNameW
title: SetupDiClassGuidsFromNameW function (setupapi.h)
description: The SetupDiClassGuidsFromName function retrieves the GUID(s) associated with the specified class name. This list is built based on the classes currently installed on the system. (Unicode)
helpviewer_keywords: ["SetupDiClassGuidsFromName", "SetupDiClassGuidsFromName function [Device and Driver Installation]", "SetupDiClassGuidsFromNameW", "devinst.setupdiclassguidsfromname", "di-rtns_6b309545-3832-4802-9668-21a107f3c651.xml", "setupapi/SetupDiClassGuidsFromName"]
old-location: devinst\setupdiclassguidsfromname.htm
tech.root: devinst
ms.assetid: 54516c6f-ec78-47ea-93f5-a4c7cde5a601
ms.date: 12/05/2018
ms.keywords: SetupDiClassGuidsFromName, SetupDiClassGuidsFromName function [Device and Driver Installation], SetupDiClassGuidsFromNameA, SetupDiClassGuidsFromNameW, devinst.setupdiclassguidsfromname, di-rtns_6b309545-3832-4802-9668-21a107f3c651.xml, setupapi/SetupDiClassGuidsFromName
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
 - SetupDiClassGuidsFromNameW
 - setupapi/SetupDiClassGuidsFromNameW
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
 - SetupDiClassGuidsFromName
 - SetupDiClassGuidsFromNameW
---

# SetupDiClassGuidsFromNameW function


## -description

The <b>SetupDiClassGuidsFromName</b> function retrieves the GUID(s) associated with the specified class name. This list is built based on the classes currently installed on the system.

## -parameters

### -param ClassName [in]

The name of the class for which to retrieve the class GUID.

### -param ClassGuidList [out]

A pointer to an array to receive the list of GUIDs associated with the specified class name.

### -param ClassGuidListSize [in]

The number of GUIDs in the <i>ClassGuidList</i> array.

### -param RequiredSize [out]

Supplies a pointer to a variable that receives the number of GUIDs associated with the class name. If this number is greater than the size of the <i>ClassGuidList</i> buffer, the number indicates how large the array must be in order to store all the GUIDs.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Call <b>SetupDiClassGuidsFromNameEx</b> to retrieve the class GUIDs for a class on a remote computer.





> [!NOTE]
> The setupapi.h header defines SetupDiClassGuidsFromName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiclassguidsfromnameexa">SetupDiClassGuidsFromNameEx</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiclassnamefromguida">SetupDiClassNameFromGuid</a>
