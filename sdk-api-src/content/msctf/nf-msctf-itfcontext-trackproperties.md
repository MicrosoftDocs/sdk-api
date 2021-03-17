---
UID: NF:msctf.ITfContext.TrackProperties
title: ITfContext::TrackProperties (msctf.h)
description: ITfContext::TrackProperties method
helpviewer_keywords: ["ITfContext interface [Text Services Framework]","TrackProperties method","ITfContext.TrackProperties","ITfContext::TrackProperties","TrackProperties","TrackProperties method [Text Services Framework]","TrackProperties method [Text Services Framework]","ITfContext interface","_tsf_itfcontext_trackproperties_ref","msctf/ITfContext::TrackProperties","tsf.itfcontext_trackproperties"]
old-location: tsf\itfcontext_trackproperties.htm
tech.root: TSF
ms.assetid: e283a45d-b585-4a26-89db-7ed706f0f593
ms.date: 12/05/2018
ms.keywords: ITfContext interface [Text Services Framework],TrackProperties method, ITfContext.TrackProperties, ITfContext::TrackProperties, TrackProperties, TrackProperties method [Text Services Framework], TrackProperties method [Text Services Framework],ITfContext interface, _tsf_itfcontext_trackproperties_ref, msctf/ITfContext::TrackProperties, tsf.itfcontext_trackproperties
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContext::TrackProperties
 - msctf/ITfContext::TrackProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfContext.TrackProperties
---

# ITfContext::TrackProperties


## -description

Obtains a special property that can enumerate multiple properties over multiple ranges.

## -parameters

### -param prgProp [in]

Contains an array of property identifiers that specify the properties to track.

### -param cProp [in]

Contains the number of property identifiers in the <i>prgProp</i> array.

### -param prgAppProp [in]

Contains an array of application property identifiers that specify the application properties to track.

### -param cAppProp [in]

Contains the number of application property identifiers in the <i>prgAppProp</i> array.

### -param ppProperty [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty">ITfReadOnlyProperty</a> interface pointer that receives the tracking property.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context object is not on a document stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>

## -remarks

This method is used to quickly identify ranges with consistent property values for multiple properties. While this method could be duplicated using only the <a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty">ITfContext::GetProperty</a> method, the TSF manager can accomplish this task more quickly.

The property obtained by this method is a VT_UNKNOWN type. This property can be used to obtain an <a href="/windows/desktop/api/msctf/nn-msctf-ienumtfpropertyvalue">IEnumTfPropertyValue</a> enumerator by calling the <b>QueryInterface</b> method with IID_IEnumTfPropertyValue. This enumerator contains property values specified by <i>prgProp</i> and <i>prgAppProp</i>.


#### Examples


```cpp

const GUID *rgGuids[2] = {  &GUID_PROP_COMPOSING,
                            &GUID_PROP_ATTRIBUTE };
HRESULT hr;
ITfReadOnlyProperty *pTrackProperty;
TF_SELECTION sel;
IEnumTfRanges *pEnumRanges;
ITfRange *pRangeValue;

// Get the tracking property. 
hr = pContext->TrackProperties(NULL, 0, rgGuids, 2, &pTrackProperty);

// Get the selection range. 
hr = pContext->GetSelection(ec, TF_DEFAULT_SELECTION, 1, &sel, &cFetched);

// Use the property from TrackProperties to get an enumeration of the ranges  
// within the selection range that have the same property values. 
hr = pTrackProperty->EnumRanges(ec, &pEnumRanges, sel.range);

// Enumerate the ranges of text. 
while(pEnumRanges->Next(1, &pRangeValue, NULL) == S_OK)
{
    VARIANT varTrackerValue;
    TF_PROPERTYVAL tfPropertyVal;
    IEnumTfPropertyValue *pEnumPropVal;

    // Get the values for this range of text. 
    hr = pTrackProperty->GetValue(ec, pRangeValue, &varTrackerValue);

    // Because pTrackProperties originates from TrackProperties, 
    // varTrackerValue can be identified as a VT_UNKNOWN/IEnumTfPropertyValue. 
    varTrackerValue.punkVal->QueryInterface(    IID_IEnumTfPropertyValue,
                                                (void **)&pEnumPropVal);

    while(pEnumPropVal->Next(1, &tfPropertyVal, NULL) == S_OK)
    {
        BOOL fComposingValue;
        TfGuidAtom gaDispAttrValue;
        
        // Is this the composition property? 
        if (IsEqualGUID(tfPropertyVal.guidId, GUID_PROP_COMPOSING))
        {
            fComposingValue = (BOOL)tfPropertyVal.varValue.lVal;
        }
        // Or is this the attribute property? 
        else if (IsEqualGUID(tfPropertyVal.guidId, GUID_PROP_ATTRIBUTE))
        {
            gaDispAttrValue = (TfGuidAtom)tfPropertyVal.varValue.lVal;
        }
        
        // Clear the property. 
        VariantClear(&tfPropertyVal.varValue);
    }

    // Clear the tracker property. 
    VariantClear(&varTrackerValue);

    // Release the property enumerator. 
    pEnumPropVal->Release();

    // Release the range. 
    pRangeValue->Release();
}

// Release the selection range. 
sel.range->Release();

```

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-ienumtfpropertyvalue">IEnumTfPropertyValue
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty">ITfContext::GetProperty
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty">ITfReadOnlyProperty
      </a>