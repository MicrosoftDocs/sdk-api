---
UID: NF:msi.MsiEnumComponentsA
title: MsiEnumComponentsA function (msi.h)
description: The MsiEnumComponents function enumerates the installed components for all products. This function retrieves one component code each time it is called. (ANSI)
helpviewer_keywords: ["MsiEnumComponentsA", "msi/MsiEnumComponentsA"]
old-location: setup\msienumcomponents.htm
tech.root: setup
ms.assetid: 8ca07b2a-7616-4b0d-be3e-3e500172e5ab
ms.date: 12/05/2018
ms.keywords: MsiEnumComponents, MsiEnumComponents function, MsiEnumComponentsA, MsiEnumComponentsW, _msi_msienumcomponents, msi/MsiEnumComponents, msi/MsiEnumComponentsA, msi/MsiEnumComponentsW, setup.msienumcomponents
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiEnumComponentsW (Unicode) and MsiEnumComponentsA (ANSI)
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
 - MsiEnumComponentsA
 - msi/MsiEnumComponentsA
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
 - MsiEnumComponents
 - MsiEnumComponentsA
 - MsiEnumComponentsW
---

# MsiEnumComponentsA function


## -description

The 
<b>MsiEnumComponents</b> function enumerates the installed components for all products. This function retrieves one component code each time it is called.

## -parameters

### -param iComponentIndex [in]

Specifies the index of the component to retrieve. This parameter should be zero for the first call to the 
<b>MsiEnumComponents</b> function and then incremented for subsequent calls. Because components are not ordered, any new component has an arbitrary index. This means that the function can return components in any order.

### -param lpComponentBuf [out]

Pointer to a buffer that receives the component code. This buffer must be 39 characters long. The first 38 characters are for the 
<a href="/windows/desktop/Msi/guid">GUID</a>, and the last character is for the terminating null character.

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
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no components to return.

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
</table>
 


<div> </div>

## -remarks

To enumerate components, an application should initially call the 
<b>MsiEnumComponents</b> function with the <i>iComponentIndex</i> parameter set to zero. The application should then increment the <i>iComponentIndex</i> parameter and call 
<b>MsiEnumComponents</b> until there are no more components (that is, until the function returns ERROR_NO_MORE_ITEMS).

When making multiple calls to 
<b>MsiEnumComponents</b> to enumerate all of the product's components, each call should be made from the same thread.





> [!NOTE]
> The msi.h header defines MsiEnumComponents as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">System Status Functions</a>
