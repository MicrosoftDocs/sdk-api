---
UID: NF:mswmdm.IWMDMDevice3.GetFormatCapability
title: IWMDMDevice3::GetFormatCapability
author: windows-sdk-content
description: The GetFormatCapability method retrieves device support for files of a specified format. The capabilities are expressed as supported properties and their allowed values.
old-location: wmdm\iwmdmdevice3_getformatcapability.htm
tech.root: WMDM
ms.assetid: 728df998-748b-4c53-b5a6-3a6ccae0d7e4
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetFormatCapability, GetFormatCapability method [windows Media Device Manager], GetFormatCapability method [windows Media Device Manager],IWMDMDevice3 interface, IWMDMDevice3 interface [windows Media Device Manager],GetFormatCapability method, IWMDMDevice3.GetFormatCapability, IWMDMDevice3::GetFormatCapability, IWMDMDevice3GetFormatCapability, mswmdm/IWMDMDevice3::GetFormatCapability, wmdm.iwmdmdevice3_getformatcapability
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMDevice3::GetFormatCapability


## -description



The <b>GetFormatCapability</b> method retrieves device support for files of a specified format. The capabilities are expressed as supported properties and their allowed values.




## -parameters




### -param format [in]

Value from the <a href="https://msdn.microsoft.com/203d9bdf-cbbd-4d06-8292-26c8a472e2aa">WMDM_FORMATCODE</a> enumeration representing the queried format.


### -param pFormatSupport [out]

Pointer to the returned <a href="https://msdn.microsoft.com/9672173D-B11E-4DCB-BCAE-38B94FCC8B99">WMDM_FORMAT_CAPABILITY</a> structure containing supported properties and their allowed values. These values must be released by the application as described in <a href="https://msdn.microsoft.com/a431c3cb-e722-4d68-a82d-385fff067ea6">Getting Format Capabilities on Devices That Support IWMDMDevice3</a>.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



The client can obtain the list of supported formats by using the <a href="https://msdn.microsoft.com/f1c8406f-f0cb-4def-bc26-399908ecbf83">IWMDMDevice3::GetProperty</a> method to query the <b>g_wszWMDMFormatsSupported</b> device property.

For a particular format, a client can call this function to obtain the supported properties and get information about configurations of supported properties (for example, combinations of bit rate and sample rate). This information is expressed as a format capability.


#### Examples

The following function is passed a device pointer and a format code, and retrieves the device's format capabilities for that format. The function uses a custom function to clear the retrieved values. This custom function is shown in <a href="https://msdn.microsoft.com/a431c3cb-e722-4d68-a82d-385fff067ea6">Getting Format Capabilities on Devices That Support IWMDMDevice3</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Each format configuration is described by an WMDM_FORMAT_CAPABILITY enum, and
// has a WMDM_FORMAT_CAPABILITY structure describing the device capabilities for that format.
//        Each WMDM_FORMAT_CAPABILITY structure has a WMDM_PROP_CONFIG structure listing configurations.
//            Each WMDM_PROP_CONFIG has a WMDM_PROP_DESC describing a specific format configuration.
//                Each WMDM_PROP_DESC holds specific values as a range, a set, or a flag meaning all values are accepted.
HRESULT myGetFormatCaps(WMDM_FORMATCODE formatCode, IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Get a list of supported configurations for the format.
    WMDM_FORMAT_CAPABILITY formatCapList;
    hr = pDevice-&gt;GetFormatCapability(formatCode, &amp;formatCapList);
    HANDLE_HR(hr, "Got a WMDM_FORMATCODE structure in GetCaps","Couldn't get a WMDM_FORMATCODE structure in GetCaps");

    // Print out the format name.
    // TODO: Display a banner for device formats.
    PrintWMDM_FORMATCODE(formatCode); // Custom function to print out the format code.
    

    // Loop through the configurations and examine each one.
    for(UINT iConfig = 0; iConfig &lt; formatCapList.nPropConfig; iConfig++)
    {
        WMDM_PROP_CONFIG formatConfig = formatCapList.pConfigs[iConfig];

        // Preference level for this configuration (lower number means more preferred).
        // TODO: Display a banner for the preference-level output.

        // Loop through all properties for this configuration and get supported
        // values for the property. Values can be a single value, a range, 
        // or a list of enumerated values.
        for(UINT iDesc = 0; iDesc &lt; formatConfig.nPropDesc; iDesc++)
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
                        for(UINT iValue = 0; iValue &lt; list.cEnumValues; iValue++)
                        {
                            pVal = list.pValues[iValue];
                            // TODO: Display the current value.
                            PropVariantClear(&amp;pVal);
                            PropVariantInit(&amp;pVal);
                        }
                    }

                    break;
                default:
                    HANDLE_HR(E_FAIL, "Undefined configuration type in GetCaps" &lt;&lt; endl, "");
                    break;
            }
        }
    }
    // Now clear the memory used by WMDM_FORMAT_CAPABILITY.
    FreeFormatCapability(formatCapList);

e_Exit:
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/dd139816-dc8c-4e73-9a21-67287bfe6405">Discovering Device Format Capabilities</a>



<a href="https://msdn.microsoft.com/29e0ec95-c1ea-4157-b5aa-39d80fff407d">IWMDMDevice3 Interface</a>
 

 

