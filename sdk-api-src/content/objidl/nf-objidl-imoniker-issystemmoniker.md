---
UID: NF:objidl.IMoniker.IsSystemMoniker
title: IMoniker::IsSystemMoniker (objidl.h)
description: Determines whether this moniker is one of the system-provided moniker classes.
helpviewer_keywords: ["IMoniker interface [COM]","IsSystemMoniker method","IMoniker.IsSystemMoniker","IMoniker::IsSystemMoniker","IsSystemMoniker","IsSystemMoniker method [COM]","IsSystemMoniker method [COM]","IMoniker interface","_com_imoniker_issystemmoniker","com.imoniker_issystemmoniker","objidl/IMoniker::IsSystemMoniker"]
old-location: com\imoniker_issystemmoniker.htm
tech.root: com
ms.assetid: a61c0df9-786e-45e7-8b3d-f950decc596d
ms.date: 12/05/2018
ms.keywords: IMoniker interface [COM],IsSystemMoniker method, IMoniker.IsSystemMoniker, IMoniker::IsSystemMoniker, IsSystemMoniker, IsSystemMoniker method [COM], IsSystemMoniker method [COM],IMoniker interface, _com_imoniker_issystemmoniker, com.imoniker_issystemmoniker, objidl/IMoniker::IsSystemMoniker
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IMoniker::IsSystemMoniker
 - objidl/IMoniker::IsSystemMoniker
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IMoniker.IsSystemMoniker
---

# IMoniker::IsSystemMoniker


## -description

Determines whether this moniker is one of the system-provided moniker classes.

## -parameters

### -param pdwMksys [out]

A pointer to a variables that receives one of the values from the <a href="/windows/desktop/api/objidl/ne-objidl-mksys">MKSYS</a> enumeration and refers to one of the COM moniker classes. This parameter cannot be <b>NULL</b>.

## -returns

This method returns S_OK to indicate that the moniker is a system moniker, and S_FALSE otherwise.

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
New values of the <a href="/windows/desktop/api/objidl/ne-objidl-mksys">MKSYS</a> enumeration may be defined in the future; therefore, you should explicitly test for each value you are interested in.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Your implementation of this method must return MKSYS_NONE. You cannot use this function to identify your own monikers (for example, in your implementation of <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-composewith">IMoniker::ComposeWith</a>). Instead, you should use your moniker's implementation of <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid">IPersist::GetClassID</a> or use <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> to test for your own private interface.

<h3><a id="Implementation-specific_Notes"></a><a id="implementation-specific_notes"></a><a id="IMPLEMENTATION-SPECIFIC_NOTES"></a>Implementation-specific Notes</h3>
<table>
<tr>
<th>Implementation</th>
<th>Notes</th>
</tr>
<tr>
<td>Anti-moniker</td>
<td>This method returns S_OK and passes back MKSYS_ANTIMONIKER.
</td>
</tr>
<tr>
<td>Class moniker</td>
<td>This method returns S_OK and passes back MKSYS_CLASSMONIKER. 
</td>
</tr>
<tr>
<td>File moniker</td>
<td>This method returns S_OK and passes back MKSYS_CLASSMONIKER. 
</td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>This method returns S_OK and passes back MKSYS_GENERICCOMPOSITE.
</td>
</tr>
<tr>
<td>Item moniker</td>
<td>This method returns S_OK and passes back MKSYS_ITEMMONIKER.</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>This method returns S_OK and passes back MKSYS_OBJREFMONIKER. 
</td>
</tr>
<tr>
<td>Pointer moniker</td>
<td>This method returns S_OK and passes back MKSYS_POINTERMONIKER.
</td>
</tr>
<tr>
<td>URL moniker</td>
<td>This method returns S_OK and passes back MKSYS_URLMONIKER.
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>