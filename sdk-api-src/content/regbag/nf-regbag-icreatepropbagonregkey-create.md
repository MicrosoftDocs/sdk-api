---
UID: NF:regbag.ICreatePropBagOnRegKey.Create
title: ICreatePropBagOnRegKey::Create (regbag.h)
description: The Create method creates a property bag that can store information in the system registry.
helpviewer_keywords: ["Create","Create method [Microsoft TV Technologies]","Create method [Microsoft TV Technologies]","ICreatePropBagOnRegKey interface","ICreatePropBagOnRegKey interface [Microsoft TV Technologies]","Create method","ICreatePropBagOnRegKey.Create","ICreatePropBagOnRegKey::Create","ICreatePropBagOnRegKeyCreate","mstv.icreatepropbagonregkey_create","regbag/ICreatePropBagOnRegKey::Create"]
old-location: mstv\icreatepropbagonregkey_create.htm
tech.root: mstv
ms.assetid: d6410ead-7364-4db4-a4c9-cafe5fbf2e84
ms.date: 12/05/2018
ms.keywords: Create, Create method [Microsoft TV Technologies], Create method [Microsoft TV Technologies],ICreatePropBagOnRegKey interface, ICreatePropBagOnRegKey interface [Microsoft TV Technologies],Create method, ICreatePropBagOnRegKey.Create, ICreatePropBagOnRegKey::Create, ICreatePropBagOnRegKeyCreate, mstv.icreatepropbagonregkey_create, regbag/ICreatePropBagOnRegKey::Create
req.header: regbag.h
req.include-header: Tuner.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Regbag.idl
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
 - ICreatePropBagOnRegKey::Create
 - regbag/ICreatePropBagOnRegKey::Create
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - regbag.h
api_name:
 - ICreatePropBagOnRegKey.Create
---

# ICreatePropBagOnRegKey::Create


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Create</b> method creates a property bag that can store information in the system registry.

## -parameters

### -param hkey [in]

Specifies a handle to the registry key.

### -param subkey [in]

Specifies the subkey.

### -param ulOptions [in]

Reserved; must be zero.

### -param samDesired [in]

Specifies the desired access rights to the key. The value can be any combination of flags from the <i>samDesired</i> parameter in the Win32 <b>RegOpenKeyEx</b> function.

### -param iid

Specifies the interface identifier (IID) of a property bag interface. Use the value IID_IPropertyBag or IID_IPropertyBag2.

### -param ppBag [out]

Address of a variable that receives the interface specified by the <i>iid</i> parameter.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The specified IID is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>

## -remarks

This method creates a property bag and returns a pointer to the <b>IPropertyBag</b> or <b>IPropertyBag2</b> interface, depending on the value of the <i>iid</i> parameter. The returned property bag can access the specified registry key, using the access rights given in the <i>samDesired</i> parameter. The various property bag methods require different access rights, as follows:

<table>
<tr>
<th>Method
            </th>
<th>Required Access Rights
            </th>
</tr>
<tr>
<td><b>IPropertyBag::Read
            </b></td>
<td>KEY_READ</td>
</tr>
<tr>
<td><b>IPropertyBag::Write
            </b></td>
<td>KEY_WRITE</td>
</tr>
<tr>
<td><b>IPropertyBag2::CountProperties
            </b></td>
<td>KEY_QUERY_VALUE | KEY_ENUMERATE_SUB_KEYS</td>
</tr>
<tr>
<td><b>IPropertyBag2::GetPropertyInfo
            </b></td>
<td>KEY_QUERY_VALUE | KEY_ENUMERATE_SUB_KEYS</td>
</tr>
</table>
 

If you write a value of VT_EMPTY or VT_NULL the property is removed from the bag and the corresponding registry values are deleted.


#### Examples

The following example code shows how to create a read back a default tune request in the registry:


```cpp

CComPtr <ICreatePropBagOnRegKey> pCreateRegBag; 
HRESULT hr = pCreateRegBag.CoCreateInstance(CLSID_CreatePropBagOnRegKey); 
CComPtr <IPropertyBag> pRegBag; 
hr = pCreateRegBag->Create(HKEY_CURRENT_USER, 
    OLESTR("SOFTWARE\\Microsoft\\MSVidCtl\\DefaultTuneRequest"), 
    0, KEY_READ | KEY_WRITE, IID_IPropertyBag, (void**)&pRegBag); 
if(FAILED(hr)) 
{ 
  ATLASSERT(FALSE); 
  return E_FAIL; 
} 
CComPtr <IAnalogTVTuningSpace> pTuneSpace; 
hr = pTuneSpace.CoCreateInstance(CLSID_AnalogTVTuningSpace); 
if(FAILED(hr)) 
{ 
  ATLASSERT(FALSE); 
  return E_FAIL; 
} 
CComPtr<ITuneRequest> pTuneRequest; 
hr = pTuneSpace->CreateTuneRequest(&pTuneRequest); 
if(FAILED(hr)) 
{ 
  ATLASSERT(FALSE); 
  return E_FAIL; 
} 
CComQIPtr <IPersistPropertyBag> pPersist(pTuneRequest); 
CComVariant v((IUnknown*)(pTuneRequest)); 
hr = pRegBag->Write(L"tr", &v); 
if(FAILED(hr)) 
{ 
  ATLASSERT(FALSE); 
  return E_FAIL; 
} 

//restore 
CComPtr <IPropertyBag> pRegBag2; 
hr = pCreateRegBag->Create(HKEY_CURRENT_USER, 
OLESTR("SOFTWARE\\Microsoft\\MSVidCtl\\DefaultTuneRequest"),0, KEY_READ, 
IID_IPropertyBag, reinterpret_cast<void**>(&pRegBag2)); 
if(FAILED(hr)) 
{ 
  ATLASSERT(FALSE); 
  return E_FAIL; 
} 
CComVariant var; 
hr = pRegBag2->Read(OLESTR("tr"), &var, NULL); 
if(FAILED(hr)) 
{ 
  ATLASSERT(FALSE); 
  return E_FAIL; 
} 

// Make sure we have a tune request object. 
CComQIPtr<ITuneRequest> pTune; 
switch (var.vt) 
{ 
  case VT_UNKNOWN: 
    pTune = var.punkVal; 
    break; 
  case VT_DISPATCH: 
    pTune = var.pdispVal; 
    break; 
}

```


The following example loads the default tune request and returns an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a> interface pointer:


```cpp

HRESULT LoadDefaultTuneReq(ITuneRequest **ppTuneReq)
{
    HRESULT hr;
    *ppTuneReq = NULL;
    CComPtr<ICreatePropBagOnRegKey> pCreateRegBag;
    hr = pCreateRegBag.CoCreateInstance(CLSID_CreatePropBagOnRegKey, 
        NULL, CLSCTX_INPROC_SERVER);
    if (FAILED(hr)) return hr;

    //Create the property bag.
    CComPtr<IPropertyBag> pRegBag;
    hr = pCreateRegBag->Create(HKEY_CURRENT_USER,
        OLESTR("SOFTWARE\\Microsoft\\MSVidCtl"), 0, KEY_READ,
        IID_IPropertyBag, reinterpret_cast<void**>(&pRegBag));
    if (FAILED(hr)) return hr;

    // Read the default tune request from the property bag.
    CComVariant var;
    hr = pRegBag->Read(OLESTR("DefaultTuneRequest"), &var, NULL);
    if (FAILED(hr)) return hr;
    
    // Make sure we got a tune request object.
    CComQIPtr<ITuneRequest> pTune;
    switch (var.vt)
    {
    case VT_UNKNOWN:
        pTune = var.punkVal;
        break;
    case VT_DISPATCH:
        pTune = var.pdispVal;
        break;
    }
    if (pTune)
    {
        *ppTuneReq = pTune.Detach();
        return S_OK;
    }
    return E_FAIL; 
}

```

## -see-also

<a href="/previous-versions/windows/desktop/api/regbag/nn-regbag-icreatepropbagonregkey">ICreatePropBagOnRegKey Interface</a>