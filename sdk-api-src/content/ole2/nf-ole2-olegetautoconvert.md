---
UID: NF:ole2.OleGetAutoConvert
title: OleGetAutoConvert function
author: windows-sdk-content
description: Determines whether the registry is set for objects of a specified CLSID to be automatically converted to another CLSID, and if so, retrieves the new CLSID.
old-location: com\olegetautoconvert.htm
old-project: com
ms.assetid: f84e578a-d2ed-4b7b-9b7c-5d63f12d5781
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: OleGetAutoConvert, OleGetAutoConvert function [COM], _com_OleGetAutoConvert, com.olegetautoconvert, ole2/OleGetAutoConvert
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
req.typenames: QACONTROL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
-	Ext-MS-Win-COM-OLE32-l1-1-0.dll
-	Ext-MS-Win-COM-OLE32-l1-1-1.dll
-	Ext-MS-Win-COM-OLE32-l1-1-2.dll
-	ext-ms-win-com-ole32-l1-1-3.dll
-	Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
-	OleGetAutoConvert
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# OleGetAutoConvert function


## -description


Determines whether the registry is set for objects of a specified CLSID to be automatically converted to another CLSID, and if so, retrieves the new CLSID.


## -parameters




### -param clsidOld [in]

The CLSID for the object.


### -param pClsidNew [out]

A pointer to a variable to receive the new CLSID, if any. If auto-conversion for <i>clsidOld</i> is not set in the registry, <i>clsidOld</i> is returned. The <i>pClsidNew</i> parameter is never <b>NULL</b>.


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
A value was successfully returned through the <i>pclsidNew</i> parameter.

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
<dt><b>REGDB_E_KEYMISSING</b></dt>
</dl>
</td>
<td width="60%">
Auto-convert is not active or there was no registry entry for the <i>clsidOld</i> parameter.


</td>
</tr>
</table>
 




## -remarks



<b>OleGetAutoConvert</b> returns the <b><a href="https://msdn.microsoft.com/e34b799b-0d23-4034-ba79-49e92ec4dea7">AutoConvertTo</a></b> entry in the registry for the specified object. The <b>AutoConvertTo</b> subkey specifies whether objects of a given CLSID are to be automatically converted to a new CLSID. This is usually used to convert files created by older versions of an application to the current version. If there is no <b>AutoConvertTo</b> entry, this function returns the value of <i>clsidOld</i>.

The <a href="https://msdn.microsoft.com/fe470f8a-b2f0-48a4-a270-77420bd1472a">OleDoAutoConvert</a> function calls <b>OleGetAutoConvert</b> to determine whether the object specified is to be converted. A container application that supports object conversion should call <b>OleDoAutoConvert</b> each time it loads an object. If the container uses the <a href="https://msdn.microsoft.com/f2d8bb2e-5bd1-4991-a80c-ed06bfd5c9f9">OleLoad</a> helper function, it need not call <b>OleDoAutoConvert</b> explicitly because <b>OleLoad</b> calls it internally.

To set up automatic conversion of a given class, you can call the <a href="https://msdn.microsoft.com/39abf385-962a-4b20-b319-501c8130e050">OleSetAutoConvert</a> function (typically in the setup program of an application installation). This function uses the <b>AutoConvertTo</b> subkey to tag a class of objects for automatic conversion to a different class of objects. This is a subkey of the CLSID key.




## -see-also




<a href="https://msdn.microsoft.com/e34b799b-0d23-4034-ba79-49e92ec4dea7">AutoConvertTo</a>



<a href="https://msdn.microsoft.com/fe470f8a-b2f0-48a4-a270-77420bd1472a">OleDoAutoConvert</a>



<a href="https://msdn.microsoft.com/39abf385-962a-4b20-b319-501c8130e050">OleSetAutoConvert</a>
 

 

