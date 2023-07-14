---
UID: NF:tuner.ITuningSpaceContainer.put_Item
title: ITuningSpaceContainer::put_Item (tuner.h)
description: The put_Item method saves changes to an existing tuning space in the collection.
helpviewer_keywords: ["ITuningSpaceContainer interface [Microsoft TV Technologies]","put_Item method","ITuningSpaceContainer.put_Item","ITuningSpaceContainer::put_Item","ITuningSpaceContainerput_Item","mstv.ituningspacecontainer_put_item","put_Item","put_Item method [Microsoft TV Technologies]","put_Item method [Microsoft TV Technologies]","ITuningSpaceContainer interface","tuner/ITuningSpaceContainer::put_Item"]
old-location: mstv\ituningspacecontainer_put_item.htm
tech.root: mstv
ms.assetid: 44e82ec9-ffd0-4bc9-88da-b6c135cbd98f
ms.date: 12/05/2018
ms.keywords: ITuningSpaceContainer interface [Microsoft TV Technologies],put_Item method, ITuningSpaceContainer.put_Item, ITuningSpaceContainer::put_Item, ITuningSpaceContainerput_Item, mstv.ituningspacecontainer_put_item, put_Item, put_Item method [Microsoft TV Technologies], put_Item method [Microsoft TV Technologies],ITuningSpaceContainer interface, tuner/ITuningSpaceContainer::put_Item
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
 - ITuningSpaceContainer::put_Item
 - tuner/ITuningSpaceContainer::put_Item
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
 - ITuningSpaceContainer.put_Item
---

# ITuningSpaceContainer::put_Item


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Item</b> method saves changes to an existing tuning space in the collection.

## -parameters

### -param varIndex [in]

<b>VARIANT</b> that specifies the index of the tuning space.

### -param TuningSpace [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace</a> interface of the tuning space.

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
Invalid argument.

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
 

If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

An application can retrieve an existing tuning space from the collection, modify its properties by calling <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace</a> methods, and then call <b>put_Item</b> to save the changes. The unique name property on the tuning space must match the tuning space at the specified index in the collection; otherwise, the method returns E_INVALIDARG.

To add a new tuning space, use the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspacecontainer-add">ITuningSpaceContainer::Add</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer Interface</a>