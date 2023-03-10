---
UID: NF:wuapi.IUpdateCollection.Clear
title: IUpdateCollection::Clear (wuapi.h)
description: Removes all the elements from the collection. (IUpdateCollection.Clear)
helpviewer_keywords: ["Clear","Clear method [Windows Update Agent]","Clear method [Windows Update Agent]","IUpdateCollection interface","IUpdateCollection interface [Windows Update Agent]","Clear method","IUpdateCollection.Clear","IUpdateCollection::Clear","wua.iupdatecollection_clear","wuapi/IUpdateCollection::Clear"]
old-location: wua\iupdatecollection_clear.htm
tech.root: wua
ms.assetid: 53b30472-ae1b-4d29-a411-25f03e515996
ms.date: 12/05/2018
ms.keywords: Clear, Clear method [Windows Update Agent], Clear method [Windows Update Agent],IUpdateCollection interface, IUpdateCollection interface [Windows Update Agent],Clear method, IUpdateCollection.Clear, IUpdateCollection::Clear, wua.iupdatecollection_clear, wuapi/IUpdateCollection::Clear
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdateCollection::Clear
 - wuapi/IUpdateCollection::Clear
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateCollection.Clear
---

# IUpdateCollection::Clear


## -description

Removes all the elements from the collection.



## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The collection is read-only.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatecollection">IUpdateCollection</a>
