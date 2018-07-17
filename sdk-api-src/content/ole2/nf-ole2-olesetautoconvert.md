---
UID: NF:ole2.OleSetAutoConvert
title: OleSetAutoConvert function
author: windows-sdk-content
description: Specifies a CLSID for automatic conversion to a different class when an object of that class is loaded.
old-location: com\olesetautoconvert.htm
old-project: com
ms.assetid: 39abf385-962a-4b20-b319-501c8130e050
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: OleSetAutoConvert, OleSetAutoConvert function [COM], _com_OleSetAutoConvert, com.olesetautoconvert, ole2/OleSetAutoConvert
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleSetAutoConvert
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# OleSetAutoConvert function


## -description


Specifies a CLSID for automatic conversion to a different class when an object of that class is loaded.




## -parameters




### -param clsidOld [in]

The CLSID of the object class to be converted.


### -param clsidNew [in]

The CLSID of the object class that should replace <i>clsidOld</i>. This new CLSID replaces any existing auto-conversion information in the registry for <i>clsidOld</i>. If this value is CLSID_NULL, any existing auto-conversion information for <i>clsidOld</i> is removed from the registry.


## -returns



This function can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
The object was tagged successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The CLSID is not properly registered in the registry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_READREGDB</b></dt>
</dl>
</td>
<td width="60%">
Error reading from the registry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_WRITEREGDB</b></dt>
</dl>
</td>
<td width="60%">
Error writing to the registry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_KEYMISSING</b></dt>
</dl>
</td>
<td width="60%">
Cannot read a key from the registry.

</td>
</tr>
</table>
 




## -remarks



<b>OleSetAutoConvert</b> goes to the system registry, finds the <b><a href="https://msdn.microsoft.com/e34b799b-0d23-4034-ba79-49e92ec4dea7">AutoConvertTo</a></b> subkey under the CLSID specified by <i>clsidOld</i>, and sets it to <i>clsidNew</i>. This function does not validate whether an appropriate registry entry for <i>clsidNew</i> currently exists. These entries appear in the registry as subkeys of the CLSID key.

Object conversion means that the object's data is permanently associated with a new CLSID. Automatic conversion is typically specified in the setup program of a new version of an object application, so objects created by its older versions can be automatically updated to the new version.



For example, it may be necessary to convert spreadsheets that were created with earlier versions of a spreadsheet application to the new version. The spreadsheet objects from earlier versions have different CLSIDs than the new version. For each earlier version that you want automatically updated, you would call <b>OleSetAutoConvert</b> in the setup program, specifying the CLSID of the old version, and that of the new one. Then, whenever a user loads an object from a previous version, it would be automatically updated. To support automatic conversion of objects, a server that supports conversion must be prepared to manually convert objects that have the format of an earlier version of the server. Automatic conversion relies internally on this manual-conversion support.

Before setting the desired <b>AutoConvertTo</b> value, setup programs should also call <b>OleSetAutoConvert</b> to remove any existing conversion for the new class, by specifying the new class as the <i>clsidOld</i> parameter, and setting the <i>clsidNew</i> parameter to CLSID_NULL.




## -see-also




<a href="https://msdn.microsoft.com/e34b799b-0d23-4034-ba79-49e92ec4dea7">AutoConvertTo</a>



<a href="https://msdn.microsoft.com/fe470f8a-b2f0-48a4-a270-77420bd1472a">OleDoAutoConvert</a>



<a href="https://msdn.microsoft.com/f84e578a-d2ed-4b7b-9b7c-5d63f12d5781">OleGetAutoConvert</a>
 

 

