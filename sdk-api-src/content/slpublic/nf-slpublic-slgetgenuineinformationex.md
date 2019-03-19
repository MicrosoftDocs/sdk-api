---
UID: NF:slpublic.SLGetGenuineInformationEx
title: SLGetGenuineInformationEx function (slpublic.h)
author: windows-sdk-content
description: Specifies information about the genuine status of a Windows computer.
old-location: security\slgetgenuineinformationex.htm
tech.root: SecSLApi
ms.assetid: 229fd8f2-ec8c-4f34-a492-caf18e036b70
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SLGetGenuineInformationEx, SLGetGenuineInformationEx function [Security], security.slgetgenuineinformationex, slpublic/SLGetGenuineInformationEx
ms.topic: function
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Slc.lib
req.dll: Slc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Slc.dll
api_name:
 - SLGetGenuineInformationEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SLGetGenuineInformationEx function


## -description


Specifies information about the genuine status of a Windows computer.


## -parameters




### -param pAppId [in]

Type: <b>const SLID*</b>

A pointer to the application ID.


### -param pwszValueName [in]

Type: <b>PCWSTR</b>

The name associated with the value of the property to set.


### -param peDataType [out, optional]

Type: <b><a href="https://msdn.microsoft.com/245e79de-4823-4af9-926a-088e263cc802">SLDATATYPE</a>*</b>

A pointer to a value of the <a href="https://msdn.microsoft.com/245e79de-4823-4af9-926a-088e263cc802">SLDATATYPE</a> enumeration that specifies the data type in the <i>ppbValue</i> buffer.


### -param pcbValue [out]

Type: <b>UINT*</b>

A pointer to the size, in bytes, of the <i>ppbValue</i> buffer.


### -param ppbValue [out]

Type: <b>BYTE**</b>

A pointer to the genuine status retrieved.  When finished using the memory, free it by calling the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.


## -returns



Type: <b>HRESULT WINAPI</b>

If this function succeeds, it return <b>S_OK</b>.  Otherwise,  it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_NOT_SUPPORTED</b></dt>
<dt>0xC004F016</dt>
</dl>
</td>
<td width="60%">
The name of value is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_VALUE_NOT_FOUND</b></dt>
<dt>0xC004F012</dt>
</dl>
</td>
<td width="60%">
The value for the input key was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_NOT_GENUINE</b></dt>
<dt>0xC004F200</dt>
</dl>
</td>
<td width="60%">
The application licensing state is non-genuine.

</td>
</tr>
</table>
 



