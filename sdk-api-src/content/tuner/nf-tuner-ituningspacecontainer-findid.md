---
UID: NF:tuner.ITuningSpaceContainer.FindID
title: ITuningSpaceContainer::FindID (tuner.h)
description: The FindID method retrieves the ID of a specified tuning space within the collection.
helpviewer_keywords: ["FindID","FindID method [Microsoft TV Technologies]","FindID method [Microsoft TV Technologies]","ITuningSpaceContainer interface","ITuningSpaceContainer interface [Microsoft TV Technologies]","FindID method","ITuningSpaceContainer.FindID","ITuningSpaceContainer::FindID","ITuningSpaceContainerFindID","mstv.ituningspacecontainer_findid","tuner/ITuningSpaceContainer::FindID"]
old-location: mstv\ituningspacecontainer_findid.htm
tech.root: mstv
ms.assetid: 99ac47b4-4adc-4e12-b465-4db8ae20ff6d
ms.date: 12/05/2018
ms.keywords: FindID, FindID method [Microsoft TV Technologies], FindID method [Microsoft TV Technologies],ITuningSpaceContainer interface, ITuningSpaceContainer interface [Microsoft TV Technologies],FindID method, ITuningSpaceContainer.FindID, ITuningSpaceContainer::FindID, ITuningSpaceContainerFindID, mstv.ituningspacecontainer_findid, tuner/ITuningSpaceContainer::FindID
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - ITuningSpaceContainer::FindID
 - tuner/ITuningSpaceContainer::FindID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITuningSpaceContainer.FindID
---

# ITuningSpaceContainer::FindID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>FindID</b> method retrieves the ID of a specified tuning space within the collection.

## -parameters

### -param TuningSpace [in]

Pointer to the <b>ITuningSpace</b> interface of the tuning space.

### -param ID [out]

Pointer to a variable that receives the ID of the tuning space. The returned value is specific to this collection object (which represents the local system).

## -returns

Returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified tuning space is not a member of this collection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer Interface</a>