---
UID: NF:msctf.ITfContext.TrackProperties
title: ITfContext::TrackProperties
author: windows-driver-content
description: ITfContext::TrackProperties method
old-location: tsf\itfcontext_trackproperties.htm
old-project: TSF
ms.assetid: e283a45d-b585-4a26-89db-7ed706f0f593
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfContext interface [Text Services Framework],TrackProperties method, ITfContext.TrackProperties, ITfContext::TrackProperties, TrackProperties, TrackProperties method [Text Services Framework], TrackProperties method [Text Services Framework],ITfContext interface, _tsf_itfcontext_trackproperties_ref, msctf/ITfContext::TrackProperties, tsf.itfcontext_trackproperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfContext.TrackProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfContext::TrackProperties


## -description




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

Pointer to an <a href="https://msdn.microsoft.com/f4021a3d-6b86-469f-8943-770e7ef0cf99">ITfReadOnlyProperty</a> interface pointer that receives the tracking property.


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



This method is used to quickly identify ranges with consistent property values for multiple properties. While this method could be duplicated using only the <a href="https://msdn.microsoft.com/e5d76443-f767-47fb-be3a-8cbac224d299">ITfContext::GetProperty</a> method, the TSF manager can accomplish this task more quickly.

The property obtained by this method is a VT_UNKNOWN type. This property can be used to obtain an <a href="https://msdn.microsoft.com/7f99df15-777c-46eb-bff3-542eb1fcc428">IEnumTfPropertyValue</a> enumerator by calling the <b>QueryInterface</b> method with IID_IEnumTfPropertyValue. This enumerator contains property values specified by <i>prgProp</i> and <i>prgAppProp</i>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
const GUID *rgGuids[2] = {  &amp;GUID_PROP_COMPOSING,
                            &amp;GUID_PROP_ATTRIBUTE };
HRESULT hr;
ITfReadOnlyProperty *pTrackProperty;
TF_SELECTION sel;
IEnumTfRanges *pEnumRanges;
ITfRange *pRangeValue;

// Get the tracking property. 
hr = pContext-&gt;TrackProperties(NULL, 0, rgGuids, 2, &amp;pTrackProperty);

// Get the selection range. 
hr = pContext-&gt;GetSelection(ec, TF_DEFAULT_SELECTION, 1, &amp;sel, &amp;cFetched);

// Use the property from TrackProperties to get an enumeration of the ranges  
// within the selection range that have the same property values. 
hr = pTrackProperty-&gt;EnumRanges(ec, &amp;pEnumRanges, sel.range);

// Enumerate the ranges of text. 
while(pEnumRanges-&gt;Next(1, &amp;pRangeValue, NULL) == S_OK)
{
    VARIANT varTrackerValue;
    TF_PROPERTYVAL tfPropertyVal;
    IEnumTfPropertyValue *pEnumPropVal;

    // Get the values for this range of text. 
    hr = pTrackProperty-&gt;GetValue(ec, pRangeValue, &amp;varTrackerValue);

    // Because pTrackProperties originates from TrackProperties, 
    // varTrackerValue can be identified as a VT_UNKNOWN/IEnumTfPropertyValue. 
    varTrackerValue.punkVal-&gt;QueryInterface(    IID_IEnumTfPropertyValue,
                                                (void **)&amp;pEnumPropVal);

    while(pEnumPropVal-&gt;Next(1, &amp;tfPropertyVal, NULL) == S_OK)
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
        VariantClear(&amp;tfPropertyVal.varValue);
    }

    // Clear the tracker property. 
    VariantClear(&amp;varTrackerValue);

    // Release the property enumerator. 
    pEnumPropVal-&gt;Release();

    // Release the range. 
    pRangeValue-&gt;Release();
}

// Release the selection range. 
sel.range-&gt;Release();
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7f99df15-777c-46eb-bff3-542eb1fcc428">IEnumTfPropertyValue
      </a>



<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a>



<a href="https://msdn.microsoft.com/e5d76443-f767-47fb-be3a-8cbac224d299">
        ITfContext::GetProperty
      </a>



<a href="https://msdn.microsoft.com/f4021a3d-6b86-469f-8943-770e7ef0cf99">
        ITfReadOnlyProperty
      </a>
 

 

