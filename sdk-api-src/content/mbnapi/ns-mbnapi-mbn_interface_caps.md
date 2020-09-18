---
UID: NS:mbnapi.MBN_INTERFACE_CAPS
title: MBN_INTERFACE_CAPS (mbnapi.h)
description: The MBN_INTERFACE_CAPS structure represents the interface capabilities.
helpviewer_keywords: ["MBN_INTERFACE_CAPS","MBN_INTERFACE_CAPS structure [Microsoft Broadband Networks]","mbn.mbn_interface_caps","mbnapi/MBN_INTERFACE_CAPS"]
old-location: mbn\mbn_interface_caps.htm
tech.root: mbn
ms.assetid: faee7f53-b465-4240-b163-ce88fae764df
ms.date: 12/05/2018
ms.keywords: MBN_INTERFACE_CAPS, MBN_INTERFACE_CAPS structure [Microsoft Broadband Networks], mbn.mbn_interface_caps, mbnapi/MBN_INTERFACE_CAPS
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MBN_INTERFACE_CAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_INTERFACE_CAPS
 - mbnapi/MBN_INTERFACE_CAPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_INTERFACE_CAPS
---

# MBN_INTERFACE_CAPS structure


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_INTERFACE_CAPS</b> structure represents the interface capabilities.  This structure is returned by the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-getinterfacecapability">GetInterfaceCapability</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>.

## -struct-fields

### -field cellularClass

An <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_cellular_class">MBN_CELLULAR_CLASS</a> value that specifies the cellular technology used by the device.

### -field voiceClass

An <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_voice_class">MBN_VOICE_CLASS</a> value that specifies   how voice calls are handled.

### -field dataClass

A bitwise OR combination of <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_data_class">MBN_DATA_CLASS</a> values that specifies which data services are supported.  For GSM devices, only the GSM-based data services can be present, that is, only GPRS, EDGE, UMTS, LTE, and HSDPA are valid values for GSM devices.

For CDMA devices, only the CDMA-related data services will be present, that is, only 1xRTT, 1xEV-DO, and 1xEV-DO RevA are valid values for CDMA devices.  1xEV-DO RevB is reserved for future use.

This field has the bit value <b>MBN_DATA_CLASS_CUSTOM</b> set if the data class some other data class which is not defined in the enumeration is also supported by device. If <b>MBN_DATA_CLASS_CUSTOM</b> is set then information regarding custom data class is available in <i>customDataClass</i> field.

### -field customDataClass

Contains the name of the custom data class.  If the <b>MBN_DATA_CLASS_CUSTOM</b> bit  of <b>dataClass</b> is not set, then the string is <b>NULL</b>.  Otherwise, the caller must free this string by calling <a href="/windows/win32/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

### -field gsmBandClass

A bit field that specifies the frequency bands  supported by the GSM device.  <b>MBN_BAND_CLASS_I</b> through <b>MBN_BAND_CLASS_X</b> and <b>MBN_BAND_CLASS_CUSTOM</b>  are valid values.  These values are defined by <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_band_class">MBN_BAND_CLASS</a>. If <b>gsmBandClass</b> is set to <b>MBN_BAND_CLASS_CUSTOM</b>, additional information about the band class appears in <b>customBandClass</b>.

The following table provides additional information about  the <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_band_class">MBN_BAND_CLASS</a> values. 

<table>
<tr>
<th>MBN_BAND_CLASS Value</th>
<th>Designated spectrum</th>
<th>Industry name</th>
<th>Uplink (MS to BTS)</th>
<th>Downlink (BTS to MS)</th>
<th>Regions</th>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_I</b></td>
<td>UMTS2100</td>
<td>IMT</td>
<td>1920-1980</td>
<td>2110-2170</td>
<td>Europe, Korea, Japan China</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_II</b></td>
<td>UMT21900</td>
<td>PCS1900</td>
<td>1850-1910</td>
<td>1930-1990</td>
<td>North America, Latin America</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_III</b></td>
<td>UMTS1800</td>
<td>DCS1800</td>
<td>1710-1785</td>
<td>1805-1880</td>
<td>Europe, China</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_IV</b></td>
<td>AWS</td>
<td>AWS, 1.7/2.1</td>
<td>1710-1785</td>
<td>2110-2155</td>
<td>North America, Latin America</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_V</b></td>
<td>UMTS850</td>
<td>GSM850</td>
<td>824-849</td>
<td>869-894</td>
<td>North America, Latin America</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_VI</b></td>
<td>UMTS800</td>
<td>UMTS800</td>
<td>830-840</td>
<td>875-885</td>
<td>Japan</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_VII</b></td>
<td>UMTS2600</td>
<td>UMTS2600</td>
<td>2500-2570</td>
<td>2620-2690</td>
<td>Europe</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_VIII</b></td>
<td>UMTS900</td>
<td>EGSM900</td>
<td>880-915</td>
<td>925-960</td>
<td>Europe, China</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_IX</b></td>
<td>UMTS1700</td>
<td>UMTS1700</td>
<td>1750-1770</td>
<td>1845-1880</td>
<td>Japan</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_X</b></td>
<td></td>
<td></td>
<td>1710-1770</td>
<td>2110-2170</td>
<td></td>
</tr>
</table>

### -field cdmaBandClass

A bit field that specifies the frequency bands supported by the CDMA device.  <b>MBN_BAND_CLASS_0</b> through <b>MBN_BAND_CLASS_XVII</b>, <b>MBN_BAND_CLASS_NONE</b>, and  <b>MBN_BAND_CLASS_CUSTOM</b> are valid values.  These values are defined by <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_band_class">MBN_BAND_CLASS</a>.  If <b>cdmaBandClass</b> is set to <b>MBN_BAND_CLASS_CUSTOM</b>, additional information about the band class appears in <b>customBandClass</b>. 

The following table provides additional information about MBN_BAND_CLASS values.

<table>
<tr>
<th>MBN_BAND_CLASS Value</th>
<th>Industry Name</th>
<th>Uplink (MS to BTS)</th>
<th>Downlink (BTS to MS)</th>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_0</b></td>
<td>800MHx Cellular</td>
<td>824.025.844.995</td>
<td>869.025.889.995</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_I</b></td>
<td>1900MHz Band</td>
<td>1850-1910</td>
<td>1930-1990</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_II</b></td>
<td>TACS Band</td>
<td>872.025.914.9875</td>
<td>917.0125.959.9875</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_III</b></td>
<td>JTACS Band</td>
<td>887.0125.924.9875</td>
<td>832.0125.869.9875</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_IV</b></td>
<td>Korean PCS Band</td>
<td>1750-1780</td>
<td>1840-1870</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_V</b></td>
<td>450 MHz Band</td>
<td>410-483.475</td>
<td>420-493.475</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_VI</b></td>
<td>2 GHz Band</td>
<td>1920-1979.950</td>
<td>2110-2169.950</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_VII</b></td>
<td>700 MHz Band</td>
<td>776-794</td>
<td>746-764</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_VIII</b></td>
<td>1800 MHz Band</td>
<td>1710-1784.950</td>
<td>1805-1879.95</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_IX</b></td>
<td>900 MHz Band</td>
<td>880-914-950</td>
<td>925-959.950</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_X</b></td>
<td>Secondary 800 MHz Band</td>
<td>806-900.975</td>
<td>851-939.975</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_XI</b></td>
<td>400 MHz European PAMR Band</td>
<td>410-483.475</td>
<td>420-493.475</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_XII</b></td>
<td>800 MHz PAMR Band</td>
<td>870.125-875.9875</td>
<td>915.0125-920.9875</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_XIII</b></td>
<td>2.5 GHz IMT200 Extension Band</td>
<td>2500-2570</td>
<td>2620-2690</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_XIV</b></td>
<td>US PCS 1.9 GHz Band</td>
<td>1850-1915</td>
<td>1930-1995</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_XV</b></td>
<td>AWS Band</td>
<td>1710-1755</td>
<td>2110-2155</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_XVI</b></td>
<td>US 2.5 GHz Band</td>
<td>2502-2568</td>
<td>2624-2690</td>
</tr>
<tr>
<td><b>MBN_BAND_CLASS_XVII</b></td>
<td>US 2.5 GHz Forward Link Only Band</td>
<td></td>
<td>2624-2690</td>
</tr>
</table>

### -field customBandClass

Contains the name of the custom band class.  If the <b>MBN_BAND_CLASS_CUSTOM</b> bit  of <b>cdmaBandClass</b> and <b>gsmBandClass</b> is not set, then the string is <b>NULL</b>.  Otherwise, the caller must free this string by calling <a href="/windows/win32/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

### -field smsCaps

A bitwise OR combination of <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_sms_caps">MBN_SMS_CAPS</a> values that specifies the SMS capabilities.

### -field controlCaps

A bitwise OR combination of <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_ctrl_caps">MBN_CTRL_CAPS</a> values that represents the Mobile Broadband control capabilities for this interface.

### -field deviceID

Contains the device ID.  For GSM devices, this must be the IMEI (up to 15 digits).  For CDMA devices, this must be the ESN (11 digits) / MEID (17 digits).  The maximum length of the string is <b>MBN_DEVICEID_LEN</b>.  For the definition of <b>MBN_DEVICEID_LEN</b>, see <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_interface_caps_constants">MBN_INTERFACE_CAPS_CONSTANTS</a>.  The caller must free this string by calling <a href="/windows/win32/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

### -field manufacturer

Contains the name of the device manufacturer.  This string can be empty.  The maximum length of the string is <b>MBN_MANUFACTURER_LEN</b>.  For the definition of <b>MBN_MANUFACTURER_LEN</b>, see <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_interface_caps_constants">MBN_INTERFACE_CAPS_CONSTANTS</a>.  The caller must free this string by calling <a href="/windows/win32/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

### -field model

Contains the device model.  This string can be empty.  The maximum length of this string is <b>MBN_MODEL_LEN</b>.  For the definition of <b>MBN_MODEL_LEN</b>, see <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_interface_caps_constants">MBN_INTERFACE_CAPS_CONSTANTS</a>.  The caller must free this string by calling <a href="/windows/win32/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

### -field firmwareInfo

Contains the firmware-specific information for this device.  This string can be empty.  The maximum length of the string is <b>MBN_FIRMWARE_LEN</b>.  For the definition of <b>MBN_FIRMWARE_LEN</b>, see <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_interface_caps_constants">MBN_INTERFACE_CAPS_CONSTANTS</a>.  The caller must free this string by calling <a href=" http://msdn.microsoft.com/en-us/library/ms221481.aspx">SysFreeString</a>.