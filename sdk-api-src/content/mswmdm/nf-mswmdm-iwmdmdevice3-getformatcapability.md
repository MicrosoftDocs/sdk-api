---
UID: NF:mswmdm.IWMDMDevice3.GetFormatCapability
title: IWMDMDevice3::GetFormatCapability (mswmdm.h)
description: The GetFormatCapability method retrieves device support for files of a specified format. The capabilities are expressed as supported properties and their allowed values.
helpviewer_keywords: ["GetFormatCapability","GetFormatCapability method [windows Media Device Manager]","GetFormatCapability method [windows Media Device Manager]","IWMDMDevice3 interface","IWMDMDevice3 interface [windows Media Device Manager]","GetFormatCapability method","IWMDMDevice3.GetFormatCapability","IWMDMDevice3::GetFormatCapability","IWMDMDevice3GetFormatCapability","mswmdm/IWMDMDevice3::GetFormatCapability","wmdm.iwmdmdevice3_getformatcapability"]
old-location: wmdm\iwmdmdevice3_getformatcapability.htm
tech.root: WMDM
ms.assetid: 728df998-748b-4c53-b5a6-3a6ccae0d7e4
ms.date: 12/05/2018
ms.keywords: GetFormatCapability, GetFormatCapability method [windows Media Device Manager], GetFormatCapability method [windows Media Device Manager],IWMDMDevice3 interface, IWMDMDevice3 interface [windows Media Device Manager],GetFormatCapability method, IWMDMDevice3.GetFormatCapability, IWMDMDevice3::GetFormatCapability, IWMDMDevice3GetFormatCapability, mswmdm/IWMDMDevice3::GetFormatCapability, wmdm.iwmdmdevice3_getformatcapability
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMDevice3::GetFormatCapability
 - mswmdm/IWMDMDevice3::GetFormatCapability
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMDevice3.GetFormatCapability
---

# IWMDMDevice3::GetFormatCapability


## -description

The <b>GetFormatCapability</b> method retrieves device support for files of a specified format. The capabilities are expressed as supported properties and their allowed values.

## -parameters

### -param format [in]

Value from the <a href="/windows/desktop/WMDM/wmdm-formatcode">WMDM_FORMATCODE</a> enumeration representing the queried format.

### -param pFormatSupport [out]

Pointer to the returned <a href="/windows/desktop/WMDM/wmdm-format-capability">WMDM_FORMAT_CAPABILITY</a> structure containing supported properties and their allowed values. These values must be released by the application as described in <a href="/windows/desktop/WMDM/getting-format-capabilities-on-devices-that-support-iwmdmdevice3">Getting Format Capabilities on Devices That Support IWMDMDevice3</a>.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The client can obtain the list of supported formats by using the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty">IWMDMDevice3::GetProperty</a> method to query the <b>g_wszWMDMFormatsSupported</b> device property.

For a particular format, a client can call this function to obtain the supported properties and get information about configurations of supported properties (for example, combinations of bit rate and sample rate). This information is expressed as a format capability.


#### Examples

The following function is passed a device pointer and a format code, and retrieves the device's format capabilities for that format. The function uses a custom function to clear the retrieved values. This custom function is shown in <a href="/windows/desktop/WMDM/getting-format-capabilities-on-devices-that-support-iwmdmdevice3">Getting Format Capabilities on Devices That Support IWMDMDevice3</a>.


```cpp

// Each format configuration is described by a WMDM_FORMAT_CAPABILITY enum, and
// has a WMDM_FORMAT_CAPABILITY structure describing the device capabilities for that format.
//        Each WMDM_FORMAT_CAPABILITY structure has a WMDM_PROP_CONFIG structure listing configurations.
//            Each WMDM_PROP_CONFIG has a WMDM_PROP_DESC describing a specific format configuration.
//                Each WMDM_PROP_DESC holds specific values as a range, a set, or a flag meaning all values are accepted.
HRESULT myGetFormatCaps(WMDM_FORMATCODE formatCode, IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Get a list of supported configurations for the format.
    WMDM_FORMAT_CAPABILITY formatCapList;
    hr = pDevice->GetFormatCapability(formatCode, &formatCapList);
    HANDLE_HR(hr, "Got a WMDM_FORMATCODE structure in GetCaps","Couldn't get a WMDM_FORMATCODE structure in GetCaps");

    // Print out the format name.
    // TODO: Display a banner for device formats.
    PrintWMDM_FORMATCODE(formatCode); // Custom function to print out the format code.
    

    // Loop through the configurations and examine each one.
    for(UINT iConfig = 0; iConfig < formatCapList.nPropConfig; iConfig++)
    {
        WMDM_PROP_CONFIG formatConfig = formatCapList.pConfigs[iConfig];

        // Preference level for this configuration (lower number means more preferred).
        // TODO: Display a banner for the preference-level output.

        // Loop through all properties for this configuration and get supported
        // values for the property. Values can be a single value, a range, 
        // or a list of enumerated values.
        for(UINT iDesc = 0; iDesc < formatConfig.nPropDesc; iDesc++)
        {
            WMDM_PROP_DESC propDesc = formatConfig.pPropDesc[iDesc];
            // TODO: Display the property name.

            // Three ways a value can be represented: any, a range, or a list.
            switch (propDesc.ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // TODO: Display a message indicating that all values are valid.
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    {
                        // List these in the docs as the propvariants set.
                        WMDM_PROP_VALUES_RANGE rng = propDesc.ValidValues.ValidValuesRange;
                        // TODO: Display a banner for the values to follow
                        // TODO: Display the max value.
                        // TODO: Display the min value.
                        // TODO: Display the step value.
                    }
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    {
                        // TODO: Display a banner for the values to follow.
                        WMDM_PROP_VALUES_ENUM list = propDesc.ValidValues.EnumeratedValidValues;
                        PROPVARIANT pVal;
                        for(UINT iValue = 0; iValue < list.cEnumValues; iValue++)
                        {
                            pVal = list.pValues[iValue];
                            // TODO: Display the current value.
                            PropVariantClear(&pVal);
                            PropVariantInit(&pVal);
                        }
                    }

                    break;
                default:
                    HANDLE_HR(E_FAIL, "Undefined configuration type in GetCaps" << endl, "");
                    break;
            }
        }
    }
    // Now clear the memory used by WMDM_FORMAT_CAPABILITY.
    FreeFormatCapability(formatCapList);

e_Exit:
    return hr;
}

```

## -see-also

<a href="/windows/desktop/WMDM/discovering-device-format-capabilities">Discovering Device Format Capabilities</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3">IWMDMDevice3 Interface</a>