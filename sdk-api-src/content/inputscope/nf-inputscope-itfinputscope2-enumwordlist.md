---
UID: NF:inputscope.ITfInputScope2.EnumWordList
title: ITfInputScope2::EnumWordList (inputscope.h)
description: ITfInputScope2::EnumWordList method
helpviewer_keywords: ["EnumWordList","EnumWordList method [Text Services Framework]","EnumWordList method [Text Services Framework]","ITfInputScope2 interface","ITfInputScope2 interface [Text Services Framework]","EnumWordList method","ITfInputScope2.EnumWordList","ITfInputScope2::EnumWordList","_tsf_itfinputscope2_enumwordlist_ref","inputscope/ITfInputScope2::EnumWordList","tsf.itfinputscope2_enumwordlist"]
old-location: tsf\itfinputscope2_enumwordlist.htm
tech.root: TSF
ms.assetid: 89379dab-6f96-4a86-8433-b6b0a8e45516
ms.date: 12/05/2018
ms.keywords: EnumWordList, EnumWordList method [Text Services Framework], EnumWordList method [Text Services Framework],ITfInputScope2 interface, ITfInputScope2 interface [Text Services Framework],EnumWordList method, ITfInputScope2.EnumWordList, ITfInputScope2::EnumWordList, _tsf_itfinputscope2_enumwordlist_ref, inputscope/ITfInputScope2::EnumWordList, tsf.itfinputscope2_enumwordlist
req.header: inputscope.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: InputScope.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfInputScope2::EnumWordList
 - inputscope/ITfInputScope2::EnumWordList
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
 - ITfInputScope2.EnumWordList
---

# ITfInputScope2::EnumWordList


## -description

Return a pointer to obtain the IEnumString interface pointer.

## -parameters

### -param ppEnumString [out]

A pointer to obtain the IEnumString interface pointer.

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

