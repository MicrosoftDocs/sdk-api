---
UID: NF:msimeapi.IImePlugInDictDictionaryList.GetDictionariesInUse
title: IImePlugInDictDictionaryList::GetDictionariesInUse
author: windows-sdk-content
description: Obtains the list of Dictionay IDs (GUID) of the IME plug-in dictionaries which are in use by IME, with their creation dates and encryption flags.
old-location: intl\iimeplugindictdictionarylist_getdictionariesinuse.htm
tech.root: Intl
ms.assetid: 145F403E-7A7D-4336-96CD-620FA61DFCBF
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDictionariesInUse, GetDictionariesInUse method [Internationalization for Windows Applications], GetDictionariesInUse method [Internationalization for Windows Applications],IImePlugInDictDictionaryList interface, IImePlugInDictDictionaryList interface [Internationalization for Windows Applications],GetDictionariesInUse method, IImePlugInDictDictionaryList.GetDictionariesInUse, IImePlugInDictDictionaryList::GetDictionariesInUse, intl.iimeplugindictdictionarylist_getdictionariesinuse, msimeapi/IImePlugInDictDictionaryList::GetDictionariesInUse
ms.topic: method
req.header: msimeapi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msimeapi.h
api_name:
 - IImePlugInDictDictionaryList.GetDictionariesInUse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IImePlugInDictDictionaryList::GetDictionariesInUse


## -description


Obtains the list of Dictionay IDs (<b>GUID</b>) of the IME plug-in dictionaries which are in use by IME, with their creation dates and encryption flags.


## -parameters




### -param prgDictionaryGUID [out]

Array of the dictionary IDs (<b>GUID</b>) of the IME plug-in dictionaries which are in use by IME.


### -param prgDateCreated [in, out]

Array of the dates of creation for each of the IME plug-in dictionaries returned by <i>prgDictionaryGUID</i>.


### -param prgfEncrypted [in, out]

Array of flags indicating whether each dictionary is encrypted or not for each of the IME plug-in dictionaries returned by <i>prgDictionaryGUID</i>.


## -returns



This method can return one of these values.

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
Succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Other errors.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/EF14E963-26DF-4E72-9BDF-3AE99D0B7273">IImePlugInDictDictionaryList</a>
 

 

