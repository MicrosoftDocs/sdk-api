---
UID: NF:msi.MsiGetProductPropertyA
title: MsiGetProductPropertyA function (msi.h)
description: The MsiGetProductProperty function retrieves product properties. These properties are in the product database. (ANSI)
helpviewer_keywords: ["MsiGetProductPropertyA", "msi/MsiGetProductPropertyA"]
old-location: setup\msigetproductproperty.htm
tech.root: setup
ms.assetid: 724f6034-c492-4bab-97dc-d9b2f75e9642
ms.date: 12/05/2018
ms.keywords: MsiGetProductProperty, MsiGetProductProperty function, MsiGetProductPropertyA, MsiGetProductPropertyW, _msi_msigetproductproperty, msi/MsiGetProductProperty, msi/MsiGetProductPropertyA, msi/MsiGetProductPropertyW, setup.msigetproductproperty
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetProductPropertyW (Unicode) and MsiGetProductPropertyA (ANSI)
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
 - MsiGetProductPropertyA
 - msi/MsiGetProductPropertyA
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
 - MsiGetProductProperty
 - MsiGetProductPropertyA
 - MsiGetProductPropertyW
---

# MsiGetProductPropertyA function


## -description

The 
<b>MsiGetProductProperty</b> function retrieves product properties. These properties are in the product database.

## -parameters

### -param hProduct [in]

Handle to the product obtained from 
<a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.

### -param szProperty [in]

Specifies the property to retrieve. This is case-sensitive.

### -param lpValueBuf [out]

Pointer to a buffer that receives the property value. The value is truncated and null-terminated if <i>lpValueBuf</i> is too small. This parameter can be null.

### -param pcchValueBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpValueBuf</i> parameter. On input, this is the full size of the buffer, including a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character. 




If <i>lpValueBuf</i> is null, <i>pcchValueBuf</i> can be null.

## -returns

The 
					<b>MsiGetProductProperty</b> function return the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
An invalid handle was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
A buffer is too small to hold the entire property value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

When the 
<b>MsiGetProductProperty</b> function returns, the <i>pcchValueBuf</i> parameter contains the length of the string stored in the buffer. The count returned does not include the terminating null character. If the buffer is not big enough, 
<b>MsiGetProductProperty</b> returns ERROR_MORE_DATA, and 
<b>MsiGetProductProperty</b> contains the size of the string, in characters, without counting the null character.





> [!NOTE]
> The msi.h header defines MsiGetProductProperty as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Product Query Functions</a>
