---
UID: NF:devicetopology.IPartsList.GetCount
title: IPartsList::GetCount (devicetopology.h)
description: The GetCount method gets the number of parts in the parts list.
helpviewer_keywords: ["GetCount","GetCount method [Core Audio]","GetCount method [Core Audio]","IPartsList interface","IPartsList interface [Core Audio]","GetCount method","IPartsList.GetCount","IPartsList::GetCount","IPartsListGetCount","coreaudio.ipartslist_getcount","devicetopology/IPartsList::GetCount"]
old-location: coreaudio\ipartslist_getcount.htm
tech.root: CoreAudio
ms.assetid: 78ca8592-f687-4194-873b-83640c6e72da
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [Core Audio], GetCount method [Core Audio],IPartsList interface, IPartsList interface [Core Audio],GetCount method, IPartsList.GetCount, IPartsList::GetCount, IPartsListGetCount, coreaudio.ipartslist_getcount, devicetopology/IPartsList::GetCount
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IPartsList::GetCount
 - devicetopology/IPartsList::GetCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IPartsList.GetCount
---

# IPartsList::GetCount


## -description

The <b>GetCount</b> method gets the number of parts in the parts list.

## -parameters

### -param pCount [out]

Pointer to a <b>UINT</b> variable into which the method writes the parts count (the number of parts in the parts list).

## -returns

If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pCount</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipartslist">IPartsList Interface</a>