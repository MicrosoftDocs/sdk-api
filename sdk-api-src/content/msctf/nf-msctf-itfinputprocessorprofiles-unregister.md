---
UID: NF:msctf.ITfInputProcessorProfiles.Unregister
title: ITfInputProcessorProfiles::Unregister (msctf.h)
description: ITfInputProcessorProfiles::Unregister method
helpviewer_keywords: ["ITfInputProcessorProfiles interface [Text Services Framework]","Unregister method","ITfInputProcessorProfiles.Unregister","ITfInputProcessorProfiles::Unregister","Unregister","Unregister method [Text Services Framework]","Unregister method [Text Services Framework]","ITfInputProcessorProfiles interface","_tsf_itfinputprocessorprofiles_unregister_ref","msctf/ITfInputProcessorProfiles::Unregister","tsf.itfinputprocessorprofiles_unregister"]
old-location: tsf\itfinputprocessorprofiles_unregister.htm
tech.root: TSF
ms.assetid: 53de09dd-3d99-4968-8861-397b67daf8c5
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfiles interface [Text Services Framework],Unregister method, ITfInputProcessorProfiles.Unregister, ITfInputProcessorProfiles::Unregister, Unregister, Unregister method [Text Services Framework], Unregister method [Text Services Framework],ITfInputProcessorProfiles interface, _tsf_itfinputprocessorprofiles_unregister_ref, msctf/ITfInputProcessorProfiles::Unregister, tsf.itfinputprocessorprofiles_unregister
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
 - ITfInputProcessorProfiles::Unregister
 - msctf/ITfInputProcessorProfiles::Unregister
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
 - ITfInputProcessorProfiles.Unregister
---

# ITfInputProcessorProfiles::Unregister


## -description

Removes a text service from TSF.

## -parameters

### -param rclsid [in]

Contains the text service CLSID to unregister.

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

