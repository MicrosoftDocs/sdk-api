---
UID: NF:msi.MsiGetPatchInfoW
title: MsiGetPatchInfoW function
author: windows-driver-content
description: The MsiGetPatchInfo function returns information about a patch.
old-location: setup\msigetpatchinfo.htm
old-project: Msi
ms.assetid: 4ff951df-5c1b-4874-9f09-f4ac23702e87
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: INSTALLPROPERTY_LOCALPACKAGE, MsiGetPatchInfo, MsiGetPatchInfo function, MsiGetPatchInfoA, MsiGetPatchInfoW, _msi_msigetpatchinfo, msi/MsiGetPatchInfo, msi/MsiGetPatchInfoA, msi/MsiGetPatchInfoW, setup.msigetpatchinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetPatchInfoW (Unicode) and MsiGetPatchInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DRM_CLIENT_VERSION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msi.dll
api_name:
-	MsiGetPatchInfo
-	MsiGetPatchInfoA
-	MsiGetPatchInfoW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# MsiGetPatchInfoW function


## -description


The 
<b>MsiGetPatchInfo</b> function returns information about a patch.


## -parameters




### -param szPatch [in]

Specifies the patch code for the patch package.


### -param szAttribute [in]

Specifies the attribute to be retrieved. 



<table>
<tr>
<th>Attribute</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_LOCALPACKAGE"></a><a id="installproperty_localpackage"></a><dl>
<dt><b>INSTALLPROPERTY_LOCALPACKAGE</b></dt>
</dl>
</td>
<td width="60%">
Local cached package.

</td>
</tr>
</table>
 


### -param lpValueBuf [out]

Pointer to a buffer that receives the property value. This parameter can be null.


### -param pcchValueBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpValueBuf</i> parameter. On input, this is the full size of the buffer, including a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character. 




If <i>lpValueBuf</i> is null, <i>pcchValueBuf</i> can be null.


## -returns




					The <b>MsiGetPatchInfo</b> function returns the following values.

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
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The patch package is not installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The property is unrecognized.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



When the 
<b>MsiGetPatchInfo</b> function returns, the <i>pcchValueBuf</i> parameter contains the length of the class string stored in the buffer. The count returned does not include the terminating null character.

If the buffer is too small to hold the requested data, 
<b>MsiGetPatchInfo</b> returns ERROR_MORE_DATA, and <i>pcchValueBuf</i> contains the number of characters copied to <i>lpValueBuf</i>, without counting the null character.




## -see-also




<a href="https://msdn.microsoft.com/850b598a-338e-4f84-8336-01e962256a08">Not Supported in Windows Installer 2.0 and earlier</a>
 

 

