---
UID: NF:infotech.IITPropList.SaveData
title: IITPropList::SaveData (infotech.h)
description: Saves the data size and data from the property list to a buffer.
helpviewer_keywords: ["IITPropList interface [HTML Help Workshop]","SaveData method","IITPropList.SaveData","IITPropList::SaveData","SaveData","SaveData method [HTML Help Workshop]","SaveData method [HTML Help Workshop]","IITPropList interface","htmlhelp.iitproplist_savedata","infotech/IITPropList::SaveData","refIITPropListSaveData"]
old-location: htmlhelp\iitproplist_savedata.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitproplistsavedata.htm
ms.date: 12/05/2018
ms.keywords: IITPropList interface [HTML Help Workshop],SaveData method, IITPropList.SaveData, IITPropList::SaveData, SaveData, SaveData method [HTML Help Workshop], SaveData method [HTML Help Workshop],IITPropList interface, htmlhelp.iitproplist_savedata, infotech/IITPropList::SaveData, refIITPropListSaveData
req.header: infotech.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IITPropList::SaveData
 - infotech/IITPropList::SaveData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Infotech.h
api_name:
 - IITPropList.SaveData
---

# IITPropList::SaveData


## -description

Saves the data size and data from the property list to a buffer.

## -parameters

### -param lpvHeader [in]

Pointer to a buffer containing the header.

### -param dwHdrSize [in]

Size of the buffer containing the header.

### -param lpvData [out]

Pointer to a buffer to fill.

### -param dwBufSize [in]

Size of the buffer to fill.

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
The property list was successfully saved.



</td>
</tr>
</table>

## -remarks

Make sure to pass a buffer large enough to hold the property list. Use <a href="/previous-versions/windows/desktop/api/infotech/nf-infotech-iitproplist-getdatasize">IITPropList::GetDataSize</a> to determine the buffer size to pass.

## -see-also

<a href="/previous-versions/windows/desktop/api/infotech/nn-infotech-iitproplist">IITPropList</a>