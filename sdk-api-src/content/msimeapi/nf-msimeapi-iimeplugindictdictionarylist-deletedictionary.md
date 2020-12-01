---
UID: NF:msimeapi.IImePlugInDictDictionaryList.DeleteDictionary
title: IImePlugInDictDictionaryList::DeleteDictionary (msimeapi.h)
description: Deletes a dictionary from the IME's plug-in dictionary list.
helpviewer_keywords: ["DeleteDictionary","DeleteDictionary method [Internationalization for Windows Applications]","DeleteDictionary method [Internationalization for Windows Applications]","IImePlugInDictDictionaryList interface","IImePlugInDictDictionaryList interface [Internationalization for Windows Applications]","DeleteDictionary method","IImePlugInDictDictionaryList.DeleteDictionary","IImePlugInDictDictionaryList::DeleteDictionary","intl.iimeplugindictdictionarylist_deletedictionary","msimeapi/IImePlugInDictDictionaryList::DeleteDictionary"]
old-location: intl\iimeplugindictdictionarylist_deletedictionary.htm
tech.root: Intl
ms.assetid: 38A17092-E545-4018-9D16-2C0406234D62
ms.date: 12/05/2018
ms.keywords: DeleteDictionary, DeleteDictionary method [Internationalization for Windows Applications], DeleteDictionary method [Internationalization for Windows Applications],IImePlugInDictDictionaryList interface, IImePlugInDictDictionaryList interface [Internationalization for Windows Applications],DeleteDictionary method, IImePlugInDictDictionaryList.DeleteDictionary, IImePlugInDictDictionaryList::DeleteDictionary, intl.iimeplugindictdictionarylist_deletedictionary, msimeapi/IImePlugInDictDictionaryList::DeleteDictionary
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IImePlugInDictDictionaryList::DeleteDictionary
 - msimeapi/IImePlugInDictDictionaryList::DeleteDictionary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msimeapi.h
api_name:
 - IImePlugInDictDictionaryList.DeleteDictionary
---

# IImePlugInDictDictionaryList::DeleteDictionary


## -description

Deletes a dictionary from the IME's plug-in dictionary list.

## -parameters

### -param bstrDictionaryGUID [in]

The dictionary ID (<b>GUID</b>) of the dictionary to be removed from the list.

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
The specified dictionary existed in the list and was successfully removed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified dictionary does not exist in the list.

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

<a href="/windows/desktop/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist">IImePlugInDictDictionaryList</a>