---
UID: NF:msvidctl.IMSVidCtl.get__InputsAvailable
title: IMSVidCtl::get__InputsAvailable (msvidctl.h)
description: The get__InputsAvailable method retrieves the input devices that are available in a specified category.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get__InputsAvailable method","IMSVidCtl.get__InputsAvailable","IMSVidCtl::get__InputsAvailable","IMSVidCtlget__InputsAvailable","get__InputsAvailable","get__InputsAvailable method [Microsoft TV Technologies]","get__InputsAvailable method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get__inputsavailable","msvidctl/IMSVidCtl::get__InputsAvailable"]
old-location: mstv\imsvidctl_get__inputsavailable.htm
tech.root: mstv
ms.assetid: 2d77eca3-aec9-423d-8d02-92e6f9ab5167
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get__InputsAvailable method, IMSVidCtl.get__InputsAvailable, IMSVidCtl::get__InputsAvailable, IMSVidCtlget__InputsAvailable, get__InputsAvailable, get__InputsAvailable method [Microsoft TV Technologies], get__InputsAvailable method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get__inputsavailable, msvidctl/IMSVidCtl::get__InputsAvailable
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
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
 - IMSVidCtl::get__InputsAvailable
 - msvidctl/IMSVidCtl::get__InputsAvailable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.get__InputsAvailable
---

# IMSVidCtl::get__InputsAvailable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get__InputsAvailable</b> method retrieves the input devices that are available in a specified category.

## -parameters

### -param CategoryGuid [in]

Pointer to a GUID that specifies the category to enumerate. Supported categories include the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>KSCATEGORY_BDA_NETWORK_PROVIDER</td>
<td>BDA-compatible tuner devices.</td>
</tr>
<tr>
<td>KSCATEGORY_TVTUNER</td>
<td>Non-BDA analog tuner devices.</td>
</tr>
<tr>
<td>GUID_NULL</td>
<td>Miscellaneous devices (file source, DVD).</td>
</tr>
</table>

### -param pVal [out]

Receives an <a href="/previous-versions/windows/desktop/mstv/msvidinputdevices">IMSVidInputDevices</a> interface pointer. The caller must release the interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method returns a read-only collection of input devices. Use the returned <a href="/previous-versions/windows/desktop/mstv/msvidinputdevices">IMSVidInputDevices</a> pointer to enumerate the collection.


#### Examples

The following example enumerates the available BDA-compatible tuners and retrieves their friendly names.


```cpp

CComPtr<IMSVidInputDevices> pInputs;
hr = pVidControl->get__InputsAvailable(&KSCATEGORY_BDA_NETWORK_PROVIDER, &pInputs);
if (SUCCEEDED(hr))
{
    long lCount;
    hr = pInputs->get_Count(&lCount);
    for (long ix = 0; ix < lCount; ix++)
    {
        CComBSTR bstrName;
        CComVariant var(ix);
        CComPtr<IMSVidInputDevice> pInput;
        hr = pInputs->get_Item(var, &pInput);
        hr = pInput->get_Name(&bstrName);
        // Display the name.
    }
}


```

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_inputactive">IMSVidCtl::get_InputActive</a>