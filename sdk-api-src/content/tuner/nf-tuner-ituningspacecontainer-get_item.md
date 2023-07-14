---
UID: NF:tuner.ITuningSpaceContainer.get_Item
title: ITuningSpaceContainer::get_Item (tuner.h)
description: The get_Item method retrieves a tuning space with the specified ID.
helpviewer_keywords: ["ITuningSpaceContainer interface [Microsoft TV Technologies]","get_Item method","ITuningSpaceContainer.get_Item","ITuningSpaceContainer::get_Item","ITuningSpaceContainerget_Item","get_Item","get_Item method [Microsoft TV Technologies]","get_Item method [Microsoft TV Technologies]","ITuningSpaceContainer interface","mstv.ituningspacecontainer_get_item","tuner/ITuningSpaceContainer::get_Item"]
old-location: mstv\ituningspacecontainer_get_item.htm
tech.root: mstv
ms.assetid: 02e17867-dc72-481a-8693-68e9b0288bba
ms.date: 12/05/2018
ms.keywords: ITuningSpaceContainer interface [Microsoft TV Technologies],get_Item method, ITuningSpaceContainer.get_Item, ITuningSpaceContainer::get_Item, ITuningSpaceContainerget_Item, get_Item, get_Item method [Microsoft TV Technologies], get_Item method [Microsoft TV Technologies],ITuningSpaceContainer interface, mstv.ituningspacecontainer_get_item, tuner/ITuningSpaceContainer::get_Item
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
 - ITuningSpaceContainer::get_Item
 - tuner/ITuningSpaceContainer::get_Item
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
 - ITuningSpaceContainer.get_Item
---

# ITuningSpaceContainer::get_Item


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Item</b> method retrieves a tuning space with the specified ID.

## -parameters

### -param varIndex [in]

<b>VARIANT</b> that specifies the ID of the tuning space.

### -param TuningSpace [out]

Address of an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace</a> interface pointer that will be set to the returned interface.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

Tuning spaces are identified by ID number. The ID number is unique within the collection. The range of valid IDs is not guaranteed to be contiguous; there may be holes if tuning spaces are added and then removed.


#### Examples


```cpp

CComPtr <ITuningSpaceContainer>  pTuningSpaceContainer;
// Create the SystemTuningSpaces object (not shown).

long cCount = 0;
long ID = 1; // zero is not a valid ID.
hr = pTuningSpaceContainer->get_Count(&cCount);
if (SUCCEEDED(hr))
{
    while (cCount)
    {
        CComPtr<ITuningSpace> pTuningSpace;
        CComVariant varIndex(ID);
        hr = pITuningSpaceContainer->get_Item(varIndex, &pTuningSpace);
        if (SUCCEEDED(hr))
        {
             // pTuningSpace now points to the tuning space with this ID.
             --cCount;
        }
        ID++; // increment for the next ID.
    }
}


```

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer Interface</a>