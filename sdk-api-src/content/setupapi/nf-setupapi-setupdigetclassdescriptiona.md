---
UID: NF:setupapi.SetupDiGetClassDescriptionA
title: SetupDiGetClassDescriptionA function (setupapi.h)
description: The SetupDiGetClassDescription function retrieves the class description associated with the specified setup class GUID. (ANSI)
helpviewer_keywords: ["SetupDiGetClassDescriptionA", "di-rtns_90458b4a-959d-4344-ae06-c88cbdbbfbdf.xml"]
old-location: devinst\setupdigetclassdescription.htm
tech.root: devinst
ms.assetid: a9757c77-f873-4f75-be80-c4bd1d327299
ms.date: 12/05/2018
ms.keywords: SetupDiGetClassDescription, SetupDiGetClassDescription function [Device and Driver Installation], SetupDiGetClassDescriptionA, SetupDiGetClassDescriptionW, devinst.setupdigetclassdescription, di-rtns_90458b4a-959d-4344-ae06-c88cbdbbfbdf.xml, setupapi/SetupDiGetClassDescription
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
 - SetupDiGetClassDescriptionA
 - setupapi/SetupDiGetClassDescriptionA
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
 - SetupDiGetClassDescription
 - SetupDiGetClassDescriptionA
---

# SetupDiGetClassDescriptionA function


## -description

The <b>SetupDiGetClassDescription</b> function retrieves the class description associated with the specified setup class GUID.

## -parameters

### -param ClassGuid [in]

The GUID of the setup class whose description is to be retrieved.

### -param ClassDescription [out]

A pointer to a character buffer that receives the class description.

### -param ClassDescriptionSize [in]

The size, in characters, of the <i>ClassDescription</i> buffer.

### -param RequiredSize [out, optional]

A pointer to variable of type DWORD that receives the size, in characters, that is required to store the class description (including a NULL terminator). <i>RequiredSize</i> is always less than LINE_LEN. This parameter is optional and can be <b>NULL</b>.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Call <b>SetupDiGetClassDescriptionEx</b> to retrieve the description of a setup class installed on a remote computer.





> [!NOTE]
> The setupapi.h header defines SetupDiGetClassDescription as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuildclassinfolist">SetupDiBuildClassInfoList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdescriptionexa">SetupDiGetClassDescriptionEx</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetinfclassa">SetupDiGetINFClass</a>
