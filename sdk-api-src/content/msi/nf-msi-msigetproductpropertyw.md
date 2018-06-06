---
UID: NF:msi.MsiGetProductPropertyW
title: MsiGetProductPropertyW function
author: windows-sdk-content
description: The MsiGetProductProperty function retrieves product properties. These properties are in the product database.
old-location: setup\msigetproductproperty.htm
old-project: Msi
ms.assetid: 724f6034-c492-4bab-97dc-d9b2f75e9642
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: MsiGetProductProperty, MsiGetProductProperty function, MsiGetProductPropertyA, MsiGetProductPropertyW, _msi_msigetproductproperty, msi/MsiGetProductProperty, msi/MsiGetProductPropertyA, msi/MsiGetProductPropertyW, setup.msigetproductproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: DRM_LICENSE_ACQ_DATA
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
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiGetProductPropertyW function


## -description


The 
<b>MsiGetProductProperty</b> function retrieves product properties. These properties are in the product database.


## -parameters




### -param hProduct [in]

Handle to the product obtained from 
<a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


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




## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">Product Query Functions</a>
 

 

