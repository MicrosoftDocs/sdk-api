---
UID: NF:msctf.ITfInputProcessorProfiles.Register
title: ITfInputProcessorProfiles::Register (msctf.h)
description: ITfInputProcessorProfiles::Register method
helpviewer_keywords: ["ITfInputProcessorProfiles interface [Text Services Framework]","Register method","ITfInputProcessorProfiles.Register","ITfInputProcessorProfiles::Register","Register","Register method [Text Services Framework]","Register method [Text Services Framework]","ITfInputProcessorProfiles interface","_tsf_itfinputprocessorprofiles_register_ref","msctf/ITfInputProcessorProfiles::Register","tsf.itfinputprocessorprofiles_register"]
old-location: tsf\itfinputprocessorprofiles_register.htm
tech.root: TSF
ms.assetid: 264bc32e-60a2-4dff-a212-5682d30a769e
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfiles interface [Text Services Framework],Register method, ITfInputProcessorProfiles.Register, ITfInputProcessorProfiles::Register, Register, Register method [Text Services Framework], Register method [Text Services Framework],ITfInputProcessorProfiles interface, _tsf_itfinputprocessorprofiles_register_ref, msctf/ITfInputProcessorProfiles::Register, tsf.itfinputprocessorprofiles_register
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfInputProcessorProfiles::Register
 - msctf/ITfInputProcessorProfiles::Register
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfInputProcessorProfiles.Register
---

# ITfInputProcessorProfiles::Register


## -description

Adds a text service to Text Services Foundation (TSF).

## -parameters

### -param rclsid [in]

Contains the CLSID of the text service to register.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

