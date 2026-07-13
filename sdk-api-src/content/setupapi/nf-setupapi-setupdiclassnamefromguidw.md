---
UID: NF:setupapi.SetupDiClassNameFromGuidW
title: SetupDiClassNameFromGuidW function (setupapi.h)
description: The SetupDiClassNameFromGuid function retrieves the class name associated with a class GUID. (Unicode)
helpviewer_keywords: ["SetupDiClassNameFromGuid", "SetupDiClassNameFromGuid function [Device and Driver Installation]", "SetupDiClassNameFromGuidW", "devinst.setupdiclassnamefromguid", "di-rtns_b17476f2-25e2-48ed-be4d-53af55541056.xml", "setupapi/SetupDiClassNameFromGuid"]
old-location: devinst\setupdiclassnamefromguid.htm
tech.root: devinst
ms.assetid: e23631b4-eb7f-4a75-ac23-25d3d974a3e3
ms.date: 12/05/2018
ms.keywords: SetupDiClassNameFromGuid, SetupDiClassNameFromGuid function [Device and Driver Installation], SetupDiClassNameFromGuidA, SetupDiClassNameFromGuidW, devinst.setupdiclassnamefromguid, di-rtns_b17476f2-25e2-48ed-be4d-53af55541056.xml, setupapi/SetupDiClassNameFromGuid
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
 - SetupDiClassNameFromGuidW
 - setupapi/SetupDiClassNameFromGuidW
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
 - SetupDiClassNameFromGuid
 - SetupDiClassNameFromGuidW
---

# SetupDiClassNameFromGuidW function


## -description

The <b>SetupDiClassNameFromGuid</b> function retrieves the class name associated with a class GUID.

## -parameters

### -param ClassGuid [in]

A pointer to the class GUID for the class name to retrieve.

### -param ClassName [out]

A pointer to a buffer that receives the NULL-terminated string that contains the name of the class that is specified by the pointer in the <i>ClassGuid</i> parameter.

### -param ClassNameSize [in]

The size, in characters, of the buffer that is pointed to by the <i>ClassName</i> parameter. The maximum size, in characters, of a NULL-terminated class name is MAX_CLASS_NAME_LEN. For more information about the class name size, see the following <b>Remarks</b> section.

### -param RequiredSize [out, optional]

A pointer to a variable that receives the number of characters that are required to store the requested NULL-terminated class name. This pointer is optional and can be <b>NULL</b>.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Call <b>SetupDiClassNameFromGuidEx</b> to retrieve the name for a class on a remote computer.

<b>SetupDiClassNameFromGuid</b> does not enforce a restriction on the length of the class name that it can return. This function returns the required size for a NULL-terminated class name even if it is greater than MAX_CLASS_NAME_LEN. However, MAX_CLASS_NAME_LEN is the maximum length of a valid NULL-terminated class name. A caller should never need a buffer that is larger than MAX_CLASS_NAME_LEN. For more information about class names, see the description of the <b>Class</b> entry of an <a href="/windows-hardware/drivers/install/inf-version-section">INF Version section</a>.





> [!NOTE]
> The setupapi.h header defines SetupDiClassNameFromGuid as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiclassguidsfromnamea">SetupDiClassGuidsFromName</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiclassnamefromguidexa">SetupDiClassNameFromGuidEx</a>
