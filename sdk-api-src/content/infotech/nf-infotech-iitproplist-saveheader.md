---
UID: NF:infotech.IITPropList.SaveHeader
title: IITPropList::SaveHeader (infotech.h)
description: Saves the property ID and data type from the property list to a buffer. Only saves properties marked with a persistence state of TRUE.
helpviewer_keywords: ["IITPropList interface [HTML Help Workshop]","SaveHeader method","IITPropList.SaveHeader","IITPropList::SaveHeader","SaveHeader","SaveHeader method [HTML Help Workshop]","SaveHeader method [HTML Help Workshop]","IITPropList interface","htmlhelp.iitproplist_saveheader","infotech/IITPropList::SaveHeader","refIITPropListSaveHeader"]
old-location: htmlhelp\iitproplist_saveheader.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitproplistsaveheader.htm
ms.date: 12/05/2018
ms.keywords: IITPropList interface [HTML Help Workshop],SaveHeader method, IITPropList.SaveHeader, IITPropList::SaveHeader, SaveHeader, SaveHeader method [HTML Help Workshop], SaveHeader method [HTML Help Workshop],IITPropList interface, htmlhelp.iitproplist_saveheader, infotech/IITPropList::SaveHeader, refIITPropListSaveHeader
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
 - IITPropList::SaveHeader
 - infotech/IITPropList::SaveHeader
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
 - IITPropList.SaveHeader
---

# IITPropList::SaveHeader


## -description

Saves the property ID and data type from the property list to a buffer. Only saves properties marked with a persistence state of TRUE.

## -parameters

### -param lpvData [out]

Pointer to a buffer to fill.

### -param dwHdrSize [in]

Size of the buffer.

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

Make sure to pass a buffer large enough to hold the property list. Use <a href="/previous-versions/windows/desktop/api/infotech/nf-infotech-iitproplist-getheadersize">IITPropList::GetHeaderSize</a> to determine the buffer size to pass.

## -see-also

<a href="/previous-versions/windows/desktop/api/infotech/nn-infotech-iitproplist">IITPropList</a>