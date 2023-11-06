---
UID: NF:tuner.ITuningSpaceContainer.TuningSpacesForName
title: ITuningSpaceContainer::TuningSpacesForName (tuner.h)
description: The TuningSpacesForName method retrieves a collection of tuning spaces that match the specified name.
helpviewer_keywords: ["ITuningSpaceContainer interface [Microsoft TV Technologies]","TuningSpacesForName method","ITuningSpaceContainer.TuningSpacesForName","ITuningSpaceContainer::TuningSpacesForName","ITuningSpaceContainerTuningSpacesForName","TuningSpacesForName","TuningSpacesForName method [Microsoft TV Technologies]","TuningSpacesForName method [Microsoft TV Technologies]","ITuningSpaceContainer interface","mstv.ituningspacecontainer_tuningspacesforname","tuner/ITuningSpaceContainer::TuningSpacesForName"]
old-location: mstv\ituningspacecontainer_tuningspacesforname.htm
tech.root: mstv
ms.assetid: de16a50e-7f5d-41e5-a17f-bb6d97179e4e
ms.date: 12/05/2018
ms.keywords: ITuningSpaceContainer interface [Microsoft TV Technologies],TuningSpacesForName method, ITuningSpaceContainer.TuningSpacesForName, ITuningSpaceContainer::TuningSpacesForName, ITuningSpaceContainerTuningSpacesForName, TuningSpacesForName, TuningSpacesForName method [Microsoft TV Technologies], TuningSpacesForName method [Microsoft TV Technologies],ITuningSpaceContainer interface, mstv.ituningspacecontainer_tuningspacesforname, tuner/ITuningSpaceContainer::TuningSpacesForName
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
 - ITuningSpaceContainer::TuningSpacesForName
 - tuner/ITuningSpaceContainer::TuningSpacesForName
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
 - ITuningSpaceContainer.TuningSpacesForName
---

# ITuningSpaceContainer::TuningSpacesForName


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>TuningSpacesForName</b> method retrieves a collection of tuning spaces that match the specified name.

## -parameters

### -param Name [in]

String that contains a regular expression to match against either the friendly name or the unique name of the tuning space.

### -param NewColl [out]

Address of variable that receives an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspaces">ITuningSpaces</a> interface pointer. Use this interface to enumerate the collection. The caller must release the interface.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

The returned collection might be empty, if no tuning spaces match the name.


#### Examples


```cpp

CComPtr <ITuningSpaceContainer>  pTuningSpaceContainer;
// Create the SystemTuningSpaces object (not shown).

// Try to match any tuning spaces named "Local (something) Cable".
CComPtr<ITuningSpaces> pTunes;
CComBSTR bstrName("Local.*Cable");
hr = pITuningSpaceContainer->TuningSpacesForName(bstrName, &pTunes);
if (SUCCEEDED(hr))
{
    // Find the size of the returned collection.
    long cCount = 0;
    hr = pTunes->get_Count(&cCount);
    if (SUCCEEDED(hr) && (cCount > 0))
    {
        // Enumerate the collection.
        CComPtr<IEnumTuningSpaces> pTuneEnum;
        hr = pTunes->get_EnumTuningSpaces(&pTuneEnum);
        if (SUCCEEDED(hr))
        {
            // Use IEnumTuningSpaces to iterate through the collection.
        }
    }
}

```

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer Interface</a>