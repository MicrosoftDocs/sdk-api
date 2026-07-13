---
UID: NF:msi.MsiEnumComponentQualifiersW
title: MsiEnumComponentQualifiersW function (msi.h)
description: The MsiEnumComponentQualifiers function enumerates the advertised qualifiers for the given component. This function retrieves one qualifier each time it is called. (Unicode)
helpviewer_keywords: ["MsiEnumComponentQualifiers", "MsiEnumComponentQualifiers function", "MsiEnumComponentQualifiersW", "_msi_msienumcomponentqualifiers", "msi/MsiEnumComponentQualifiers", "msi/MsiEnumComponentQualifiersW", "setup.msienumcomponentqualifiers"]
old-location: setup\msienumcomponentqualifiers.htm
tech.root: setup
ms.assetid: f499cca3-ef24-4419-92b8-7794b3a6816b
ms.date: 12/05/2018
ms.keywords: MsiEnumComponentQualifiers, MsiEnumComponentQualifiers function, MsiEnumComponentQualifiersA, MsiEnumComponentQualifiersW, _msi_msienumcomponentqualifiers, msi/MsiEnumComponentQualifiers, msi/MsiEnumComponentQualifiersA, msi/MsiEnumComponentQualifiersW, setup.msienumcomponentqualifiers
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiEnumComponentQualifiersW (Unicode) and MsiEnumComponentQualifiersA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiEnumComponentQualifiersW
 - msi/MsiEnumComponentQualifiersW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiEnumComponentQualifiers
 - MsiEnumComponentQualifiersA
 - MsiEnumComponentQualifiersW
---

# MsiEnumComponentQualifiersW function


## -description

The 
<b>MsiEnumComponentQualifiers</b> function enumerates the advertised qualifiers for the given component. This function retrieves one qualifier each time it is called.

## -parameters

### -param szComponent [in]

Specifies component whose qualifiers are to be enumerated.

### -param iIndex [in]

Specifies the index of the qualifier to retrieve. This parameter should be zero for the first call to the 
<b>MsiEnumComponentQualifiers</b> function and then incremented for subsequent calls. Because qualifiers are not ordered, any new qualifier has an arbitrary index. This means that the function can return qualifiers in any order.

### -param lpQualifierBuf [out]

Pointer to a buffer that receives the qualifier code.

### -param pcchQualifierBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpQualifierBuf</i> parameter. On input, this size should include the terminating null character. On return, the value does not include the null character.

### -param lpApplicationDataBuf [out]

Pointer to a buffer that receives the application registered data for the qualifier. This parameter can be null.

### -param pcchApplicationDataBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpApplicationDataBuf</i> parameter. On input, this size should include the terminating null character. On return, the value does not include the null character. This parameter can be null only if the <i>lpApplicationDataBuf </i> parameter is null.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration data is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
A buffer is too small to hold the requested data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no qualifiers to return.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system does not have enough memory to complete the operation. Available with Windows Server 2003.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
A value was enumerated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_COMPONENT</b></dt>
</dl>
</td>
<td width="60%">
The specified component is unknown.

</td>
</tr>
</table>

## -remarks

To enumerate qualifiers, an application should initially call the 
<b>MsiEnumComponentQualifiers</b> function with the<i> iIndex </i> parameter set to zero. The application should then increment the <i> iIndex </i> parameter and call 
<b>MsiEnumComponentQualifiers</b> until there are no more qualifiers (that is, until the function returns ERROR_NO_MORE_ITEMS).

When 
<b>MsiEnumComponentQualifiers</b> returns, the <i>pcchQualifierBuf</i> parameter contains the length of the qualifier string stored in the buffer. The count returned does not include the terminating null character. If the buffer is not big enough, 
<b>MsiEnumComponentQualifiers</b> returns ERROR_MORE_DATA, and this parameter contains the size of the string, in characters, without counting the null character. The same mechanism applies to <i>pcchDescriptionBuf</i>.
			

When making multiple calls to 
<b>MsiEnumComponentQualifiers</b> to enumerate all of the component's advertised qualifiers, each call should be made from the same thread.





> [!NOTE]
> The msi.h header defines MsiEnumComponentQualifiers as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">System Status Functions</a>
