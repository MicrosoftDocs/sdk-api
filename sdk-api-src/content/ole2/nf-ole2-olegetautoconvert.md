---
UID: NF:ole2.OleGetAutoConvert
title: OleGetAutoConvert function (ole2.h)
description: Determines whether the registry is set for objects of a specified CLSID to be automatically converted to another CLSID, and if so, retrieves the new CLSID.
helpviewer_keywords: ["OleGetAutoConvert","OleGetAutoConvert function [COM]","_com_OleGetAutoConvert","com.olegetautoconvert","ole2/OleGetAutoConvert"]
old-location: com\olegetautoconvert.htm
tech.root: com
ms.assetid: f84e578a-d2ed-4b7b-9b7c-5d63f12d5781
ms.date: 12/05/2018
ms.keywords: OleGetAutoConvert, OleGetAutoConvert function [COM], _com_OleGetAutoConvert, com.olegetautoconvert, ole2/OleGetAutoConvert
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleGetAutoConvert
 - ole2/OleGetAutoConvert
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - Ext-MS-Win-COM-OLE32-l1-1-0.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleGetAutoConvert
req.apiset: ext-ms-win-com-ole32-l1-1-0 (introduced in Windows 8)
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

<b>OleGetAutoConvert</b> returns the <b><a href="/windows/desktop/com/autoconvertto">AutoConvertTo</a></b> entry in the registry for the specified object. The <b>AutoConvertTo</b> subkey specifies whether objects of a given CLSID are to be automatically converted to a new CLSID. This is usually used to convert files created by older versions of an application to the current version. If there is no <b>AutoConvertTo</b> entry, this function returns the value of <i>clsidOld</i>.

The <a href="/windows/desktop/api/ole2/nf-ole2-oledoautoconvert">OleDoAutoConvert</a> function calls <b>OleGetAutoConvert</b> to determine whether the object specified is to be converted. A container application that supports object conversion should call <b>OleDoAutoConvert</b> each time it loads an object. If the container uses the <a href="/windows/desktop/api/ole2/nf-ole2-oleload">OleLoad</a> helper function, it need not call <b>OleDoAutoConvert</b> explicitly because <b>OleLoad</b> calls it internally.

To set up automatic conversion of a given class, you can call the <a href="/windows/desktop/api/ole2/nf-ole2-olesetautoconvert">OleSetAutoConvert</a> function (typically in the setup program of an application installation). This function uses the <b>AutoConvertTo</b> subkey to tag a class of objects for automatic conversion to a different class of objects. This is a subkey of the CLSID key.

## -see-also

<a href="/windows/desktop/com/autoconvertto">AutoConvertTo</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oledoautoconvert">OleDoAutoConvert</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olesetautoconvert">OleSetAutoConvert</a>
