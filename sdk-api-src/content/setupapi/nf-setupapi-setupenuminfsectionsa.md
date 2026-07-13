---
UID: NF:setupapi.SetupEnumInfSectionsA
title: SetupEnumInfSectionsA function (setupapi.h)
description: The SetupEnumInfSections function retrieves section names from an INF file. (ANSI)
helpviewer_keywords: ["SetupEnumInfSectionsA", "setupapi/SetupEnumInfSectionsA"]
old-location: setup\setupenuminfsections.htm
tech.root: setup
ms.assetid: 9b19ced6-728a-48e7-9e87-03fc53f7fb72
ms.date: 12/05/2018
ms.keywords: SetupEnumInfSections, SetupEnumInfSections function [Setup API], SetupEnumInfSectionsA, SetupEnumInfSectionsW, setup.setupenuminfsections, setupapi/SetupEnumInfSections, setupapi/SetupEnumInfSectionsA, setupapi/SetupEnumInfSectionsW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupEnumInfSectionsW (Unicode) and SetupEnumInfSectionsA (ANSI)
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
 - SetupEnumInfSectionsA
 - setupapi/SetupEnumInfSectionsA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-Inf-L1-1-1.dll
api_name:
 - SetupEnumInfSections
 - SetupEnumInfSectionsA
 - SetupEnumInfSectionsW
req.apiset: ext-ms-win-setupapi-inf-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# SetupEnumInfSectionsA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The <b>SetupEnumInfSections</b> function retrieves section names from an INF file.

## -parameters

### -param InfHandle [in]

Handle to the INF file that is to be queried.

### -param Index [in]

The zero-based index of the section name to retrieve. This index may not correspond to the order of sections as they appear in the INF file.

### -param Buffer [out, optional]

Pointer to a buffer that receives the section name. You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the name. Using this technique, you can avoid errors caused by an insufficient buffer size. This parameter is optional. For more information, see the Remarks section.

### -param Size [in]

Size of the buffer pointed to by <i>ReturnBuffer</i> in characters. This number includes the terminating <b>NULL</b> character.

### -param SizeNeeded [out, optional]

Pointer to a location that receives the required size of the buffer pointed to by <i>ReturnBuffer</i>. The size is specified as the number of characters required to store the section name, including the terminating <b>NULL</b> character.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.


<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_NO_MORE_ITEMS</b> if the value of <b>EnumerationIndex</b> is greater than or equal to the number of sections names in the INF file.

## -remarks

This function can enumerate all unique section names in the INF file. If a section name appears more than once in an INF file, the function returns the name only once using a single enumeration index. To return all section names in the INF file, call the function beginning with an enumeration index of zero and then make repeated calls to the function while incrementing the index until the function returns  <b>FALSE</b> and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_NO_MORE_ITEMS</b>.  Your application should not rely on the section names being returned in any order based on the enumeration index.




> [!NOTE]
> The setupapi.h header defines SetupEnumInfSections as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
