---
UID: NF:ksproxy.IKsPropertySet.Get
title: IKsPropertySet::Get method
author: windows-driver-content
description: The Get method retrieves a property identified by a property set GUID and a property ID.
old-location: dshow\ikspropertyset_get.htm
old-project: DirectShow
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: Get method [DirectShow], Get method [DirectShow], IKsPropertySet interface, Get,IKsPropertySet.Get, IKsPropertySet, IKsPropertySet interface [DirectShow], Get method, IKsPropertySet::Get, IKsPropertySetGet, dshow.ikspropertyset_get, ksproxy/IKsPropertySet::Get
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ksproxy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WAVEFORMATEXTENSIBLE, *PWAVEFORMATEXTENSIBLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IKsPropertySet.Get
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKsPropertySet::Get method


## -description



The <b>Get</b> method retrieves a property identified by a property set GUID and a property ID.




## -parameters




### -param PropSet




### -param Id




### -param InstanceData




### -param InstanceLength




### -param PropertyData




### -param DataLength




### -param BytesReturned






#### - cbInstanceData [in]

The size of the array given in <i>pInstanceData</i>, in bytes.


#### - cbPropData [in]

The size of the array given in <i>pPropData</i>, in bytes.
          


#### - dwPropID [in]

The identifier of the property within the property set.
          


#### - guidPropSet [in]

The GUID of the property set .
          


#### - pInstanceData [in]

A pointer to an array of bytes that contains instance data for the property.
          


#### - pPropData [out]

A pointer to an array of bytes that receives the property data.
          


#### - pcbReturned [out]

Receives the number of bytes the method copies to the <i>pPropData</i> array.
          


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PROP_SET_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The property set is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PROP_ID_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The property ID is not supported for the specified property set.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  Another interface by this name exists in the dsound.h header file. The two interfaces are not compatible. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff559766">IKsControl</a> interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</div>
<div> </div>
To retrieve a property, allocate a buffer which this method will then fill in. To determine the necessary buffer size, specify <b>NULL</b> for <i>pPropData</i> and zero (0) for <i>cbPropData</i>. This method returns the necessary buffer size in <i>pcbReturned</i>.

You must include Ks.h before Ksproxy.h.


#### Examples

The following example queries a pin for its pin category, by retrieving the <b>AMPROPERTY_PIN_CATEGORY</b> property. (See <a href="https://msdn.microsoft.com/0c01bd51-353d-4f48-b33c-796f740915e2">Pin Property Set</a>.)

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin-&gt;QueryInterface(IID_PPV_ARGS(&amp;pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs-&gt;Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &amp;cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&amp;pKs);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/df26341d-f2d5-4a4e-954e-705e07415808">IKsPropertySet Interface</a>



<a href="https://msdn.microsoft.com/4b8a917f-7a6c-4433-83f4-b83ef6d26115">Property Sets</a>
 

 

