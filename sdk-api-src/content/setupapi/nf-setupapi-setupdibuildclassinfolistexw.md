---
UID: NF:setupapi.SetupDiBuildClassInfoListExW
title: SetupDiBuildClassInfoListExW function (setupapi.h)
description: The SetupDiBuildClassInfoListEx function returns a list of setup class GUIDs that includes every class installed on the local system or a remote system. (Unicode)
helpviewer_keywords: ["SetupDiBuildClassInfoListEx", "SetupDiBuildClassInfoListEx function [Device and Driver Installation]", "SetupDiBuildClassInfoListExW", "devinst.setupdibuildclassinfolistex", "di-rtns_beaf3abb-65f5-4b7a-b0a1-5b8eab484eff.xml", "setupapi/SetupDiBuildClassInfoListEx"]
old-location: devinst\setupdibuildclassinfolistex.htm
tech.root: devinst
ms.assetid: 32c6c548-79f8-41be-ad9a-5456972a16eb
ms.date: 01/30/2023
ms.keywords: SetupDiBuildClassInfoListEx, SetupDiBuildClassInfoListEx function [Device and Driver Installation], SetupDiBuildClassInfoListExA, SetupDiBuildClassInfoListExW, devinst.setupdibuildclassinfolistex, di-rtns_beaf3abb-65f5-4b7a-b0a1-5b8eab484eff.xml, setupapi/SetupDiBuildClassInfoListEx
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
 - SetupDiBuildClassInfoListExW
 - setupapi/SetupDiBuildClassInfoListExW
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
 - SetupDiBuildClassInfoListEx
 - SetupDiBuildClassInfoListExW
---

# SetupDiBuildClassInfoListExW function


## -description

The <b>SetupDiBuildClassInfoListEx</b> function returns a list of setup class GUIDs that includes every class installed on the local system or a remote system.

## -parameters

### -param Flags [in]

Flags used to control exclusion of classes from the list. If no flags are specified, all setup classes are included in the list. Can be a combination of the following values:

#### DIBCI_NOINSTALLCLASS

Exclude a class if it has the <b>NoInstallClass</b> value entry in its registry key.

#### DIBCI_NODISPLAYCLASS

Exclude a class if it has the <b>NoDisplayClass</b> value entry in its registry key.

### -param ClassGuidList [out, optional]

A pointer to a buffer that receives a list of setup class GUIDs.

### -param ClassGuidListSize [in]

Supplies the number of GUIDs in the <i>ClassGuildList</i> array.

### -param RequiredSize [out]

A pointer to a variable that receives the number of GUIDs returned. If this number is greater than the size of the <i>ClassGuidList</i>, the number indicates how large the <i>ClassGuidList</i> array must be in order to contain the list.

### -param MachineName [in, optional]

A pointer to a NULL-terminated string that contains the name of a remote computer from which to retrieve installed setup classes. This parameter is optional and can be <b>NULL</b>. If <i>MachineName</i> is <b>NULL</b>, this function builds a list of classes installed on the local computer.

> [!CAUTION]
> Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.

### -param Reserved

Must be <b>NULL</b>.


##### - Flags.DIBCI_NODISPLAYCLASS

Exclude a class if it has the <b>NoDisplayClass</b> value entry in its registry key.


##### - Flags.DIBCI_NOINSTALLCLASS

Exclude a class if it has the <b>NoInstallClass</b> value entry in its registry key.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuildclassinfolist">SetupDiBuildClassInfoList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdescriptionexa">SetupDiGetClassDescriptionEx</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupDiBuildClassInfoListEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
