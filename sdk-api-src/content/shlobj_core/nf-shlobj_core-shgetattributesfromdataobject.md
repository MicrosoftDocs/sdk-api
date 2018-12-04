---
UID: NF:shlobj_core.SHGetAttributesFromDataObject
title: SHGetAttributesFromDataObject function
author: windows-sdk-content
description: SHGetAttributesFromDataObject may be altered or unavailable.
old-location: shell\SHGetAttributesFromDataObject.htm
tech.root: shell
ms.assetid: bdc583ef-a5b6-4665-949c-50f79ace39dc
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: SHGetAttributesFromDataObject, SHGetAttributesFromDataObject function [Windows Shell], _win32_SHGetAttributesFromDataObject, shell.SHGetAttributesFromDataObject, shlobj_core/SHGetAttributesFromDataObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHGetAttributesFromDataObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHGetAttributesFromDataObject function


## -description


<p class="CCE_Message">[<b>SHGetAttributesFromDataObject</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Retrieves specified pieces of information from a system data object.


## -parameters




### -param pdo [in, optional]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

The data object from which to retrieve the information.


### -param dwAttributeMask

Type: <b>DWORD</b>

One or more of the <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">SFGAO</a> flags that indicate which pieces of information the calling application wants to retrieve.


### -param pdwAttributes [out, optional]

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> value that, when this function returns successfully, receives one or more <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">SFGAO</a> flags that indicate the attributes, among those requested, that are common to all items in <i>pdo</i>. This pointer can be <b>NULL</b> if this information is not needed.


### -param pcItems [out, optional]

Type: <b>UINT*</b>

A pointer to a <b>UINT</b> that, when this function returns successfully, receives the number of PIDLs in the data object pointed to by <i>pdo</i>. This pointer can be <b>NULL</b> if this information is not needed.


## -returns



Type: <b>HRESULT</b>

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The object is not a system data object. In this case, <i>pdwAttributes</i> is set to 0.

</td>
</tr>
</table>
 



