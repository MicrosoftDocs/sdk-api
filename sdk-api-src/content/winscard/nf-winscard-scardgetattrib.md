---
UID: NF:winscard.SCardGetAttrib
title: SCardGetAttrib function (winscard.h)
description: Retrieves the current reader attributes for the given handle. It does not affect the state of the reader, driver, or card.
helpviewer_keywords: ["SCARD_ATTR_ATR_STRING","SCARD_ATTR_CHANNEL_ID","SCARD_ATTR_CHARACTERISTICS","SCARD_ATTR_CURRENT_BWT","SCARD_ATTR_CURRENT_CLK","SCARD_ATTR_CURRENT_CWT","SCARD_ATTR_CURRENT_D","SCARD_ATTR_CURRENT_EBC_ENCODING","SCARD_ATTR_CURRENT_F","SCARD_ATTR_CURRENT_IFSC","SCARD_ATTR_CURRENT_IFSD","SCARD_ATTR_CURRENT_N","SCARD_ATTR_CURRENT_PROTOCOL_TYPE","SCARD_ATTR_CURRENT_W","SCARD_ATTR_DEFAULT_CLK","SCARD_ATTR_DEFAULT_DATA_RATE","SCARD_ATTR_DEVICE_FRIENDLY_NAME","SCARD_ATTR_DEVICE_IN_USE","SCARD_ATTR_DEVICE_SYSTEM_NAME","SCARD_ATTR_DEVICE_UNIT","SCARD_ATTR_ICC_INTERFACE_STATUS","SCARD_ATTR_ICC_PRESENCE","SCARD_ATTR_ICC_TYPE_PER_ATR","SCARD_ATTR_MAX_CLK","SCARD_ATTR_MAX_DATA_RATE","SCARD_ATTR_MAX_IFSD","SCARD_ATTR_POWER_MGMT_SUPPORT","SCARD_ATTR_PROTOCOL_TYPES","SCARD_ATTR_VENDOR_IFD_SERIAL_NO","SCARD_ATTR_VENDOR_IFD_TYPE","SCARD_ATTR_VENDOR_IFD_VERSION","SCARD_ATTR_VENDOR_NAME","SCardGetAttrib","SCardGetAttrib function [Security]","_smart_scardgetattrib","security.scardgetattrib","winscard/SCardGetAttrib"]
old-location: security\scardgetattrib.htm
tech.root: security
ms.assetid: 309ac107-175b-489e-b428-b87bc4204f34
ms.date: 12/05/2018
ms.keywords: SCARD_ATTR_ATR_STRING, SCARD_ATTR_CHANNEL_ID, SCARD_ATTR_CHARACTERISTICS, SCARD_ATTR_CURRENT_BWT, SCARD_ATTR_CURRENT_CLK, SCARD_ATTR_CURRENT_CWT, SCARD_ATTR_CURRENT_D, SCARD_ATTR_CURRENT_EBC_ENCODING, SCARD_ATTR_CURRENT_F, SCARD_ATTR_CURRENT_IFSC, SCARD_ATTR_CURRENT_IFSD, SCARD_ATTR_CURRENT_N, SCARD_ATTR_CURRENT_PROTOCOL_TYPE, SCARD_ATTR_CURRENT_W, SCARD_ATTR_DEFAULT_CLK, SCARD_ATTR_DEFAULT_DATA_RATE, SCARD_ATTR_DEVICE_FRIENDLY_NAME, SCARD_ATTR_DEVICE_IN_USE, SCARD_ATTR_DEVICE_SYSTEM_NAME, SCARD_ATTR_DEVICE_UNIT, SCARD_ATTR_ICC_INTERFACE_STATUS, SCARD_ATTR_ICC_PRESENCE, SCARD_ATTR_ICC_TYPE_PER_ATR, SCARD_ATTR_MAX_CLK, SCARD_ATTR_MAX_DATA_RATE, SCARD_ATTR_MAX_IFSD, SCARD_ATTR_POWER_MGMT_SUPPORT, SCARD_ATTR_PROTOCOL_TYPES, SCARD_ATTR_VENDOR_IFD_SERIAL_NO, SCARD_ATTR_VENDOR_IFD_TYPE, SCARD_ATTR_VENDOR_IFD_VERSION, SCARD_ATTR_VENDOR_NAME, SCardGetAttrib, SCardGetAttrib function [Security], _smart_scardgetattrib, security.scardgetattrib, winscard/SCardGetAttrib
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SCardGetAttrib
 - winscard/SCardGetAttrib
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
api_name:
 - SCardGetAttrib
---

# SCardGetAttrib function


## -description

The <b>SCardGetAttrib</b> function retrieves the current reader attributes for the given handle. It does not affect the <a href="/windows/desktop/SecGloss/s-gly">state</a> of the <a href="/windows/desktop/SecGloss/r-gly">reader</a>, driver, or <a href="/windows/desktop/SecGloss/s-gly">card</a>.

## -parameters

### -param hCard [in]

Reference value returned from <a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>.

### -param dwAttrId [in]

Identifier for the <a href="/windows/desktop/SecGloss/a-gly">attribute</a> to get. The following table lists possible values for <i>dwAttrId</i>. These values are read-only. Note that vendors may not support all attributes. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_ATR_STRING"></a><a id="scard_attr_atr_string"></a><dl>
<dt><b>SCARD_ATTR_ATR_STRING</b></dt>
</dl>
</td>
<td width="60%">
Answer to reset (ATR) string.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_CHANNEL_ID"></a><a id="scard_attr_channel_id"></a><dl>
<dt><b>SCARD_ATTR_CHANNEL_ID</b></dt>
</dl>
</td>
<td width="60%">
<b>DWORD</b> encoded as 0x<i>DDDDCCCC</i>, where <i>DDDD</i> = data channel type and <i>CCCC</i> = channel number: 




<ul>
<li>The following encodings are defined for <i>DDDD</i>:</li>
<li>0x01 serial I/O; <i>CCCC</i> is a port number.</li>
<li>0x02 parallel I/O; <i>CCCC</i> is a port number.</li>
<li>0x04 PS/2 keyboard port; <i>CCCC</i> is zero.</li>
<li>0x08 SCSI; <i>CCCC</i> is SCSI ID number.</li>
<li>0x10 IDE; <i>CCCC</i> is device number.</li>
<li>0x20 USB; <i>CCCC</i> is device number.</li>
<li>0xF<i>y</i> vendor-defined interface with <i>y</i> in the range zero through 15; <i>CCCC</i> is vendor defined.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_CHARACTERISTICS"></a><a id="scard_attr_characteristics"></a><dl>
<dt><b>SCARD_ATTR_CHARACTERISTICS</b></dt>
</dl>
</td>
<td width="60%">
<b>DWORD</b> indicating which mechanical characteristics are supported. If zero, no special characteristics are supported. Note that multiple bits can be set: 




<ul>
<li>0x00000001 Card swallowing mechanism</li>
<li>0x00000002 Card ejection mechanism</li>
<li>0x00000004 Card capture mechanism</li>
</ul>
All other values are reserved for future use (RFU).

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_CURRENT_BWT"></a><a id="scard_attr_current_bwt"></a><dl>
<dt><b>SCARD_ATTR_CURRENT_BWT</b></dt>
</dl>
</td>
<td width="60%">
Current block waiting time.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_CURRENT_CLK"></a><a id="scard_attr_current_clk"></a><dl>
<dt><b>SCARD_ATTR_CURRENT_CLK</b></dt>
</dl>
</td>
<td width="60%">
Current clock rate, in kHz.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_CURRENT_CWT"></a><a id="scard_attr_current_cwt"></a><dl>
<dt><b>SCARD_ATTR_CURRENT_CWT</b></dt>
</dl>
</td>
<td width="60%">
Current character waiting time.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_CURRENT_D"></a><a id="scard_attr_current_d"></a><dl>
<dt><b>SCARD_ATTR_CURRENT_D</b></dt>
</dl>
</td>
<td width="60%">
Bit rate conversion factor.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_CURRENT_EBC_ENCODING"></a><a id="scard_attr_current_ebc_encoding"></a><dl>
<dt><b>SCARD_ATTR_CURRENT_EBC_ENCODING</b></dt>
</dl>
</td>
<td width="60%">
Current error block control encoding. 




0 = longitudinal redundancy check (LRC)

1 = cyclical redundancy check (CRC)

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_CURRENT_F"></a><a id="scard_attr_current_f"></a><dl>
<dt><b>SCARD_ATTR_CURRENT_F</b></dt>
</dl>
</td>
<td width="60%">
Clock conversion factor.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_CURRENT_IFSC"></a><a id="scard_attr_current_ifsc"></a><dl>
<dt><b>SCARD_ATTR_CURRENT_IFSC</b></dt>
</dl>
</td>
<td width="60%">
Current byte size for information field size card.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_CURRENT_IFSD"></a><a id="scard_attr_current_ifsd"></a><dl>
<dt><b>SCARD_ATTR_CURRENT_IFSD</b></dt>
</dl>
</td>
<td width="60%">
Current byte size for information field size device.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_CURRENT_N"></a><a id="scard_attr_current_n"></a><dl>
<dt><b>SCARD_ATTR_CURRENT_N</b></dt>
</dl>
</td>
<td width="60%">
Current guard time.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_CURRENT_PROTOCOL_TYPE"></a><a id="scard_attr_current_protocol_type"></a><dl>
<dt><b>SCARD_ATTR_CURRENT_PROTOCOL_TYPE</b></dt>
</dl>
</td>
<td width="60%">
<b>DWORD</b> encoded as 0x0<i>rrrpppp</i> where <i>rrr</i> is RFU and should be 0x000. <i>pppp</i> encodes the current protocol type. Whichever bit has been set indicates which ISO protocol is currently in use. (For example, if bit zero is set, <a href="/windows/desktop/SecGloss/t-gly">T=0 protocol</a> is in effect.)

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_CURRENT_W"></a><a id="scard_attr_current_w"></a><dl>
<dt><b>SCARD_ATTR_CURRENT_W</b></dt>
</dl>
</td>
<td width="60%">
Current work waiting time.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_DEFAULT_CLK"></a><a id="scard_attr_default_clk"></a><dl>
<dt><b>SCARD_ATTR_DEFAULT_CLK</b></dt>
</dl>
</td>
<td width="60%">
Default clock rate, in kHz.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_DEFAULT_DATA_RATE"></a><a id="scard_attr_default_data_rate"></a><dl>
<dt><b>SCARD_ATTR_DEFAULT_DATA_RATE</b></dt>
</dl>
</td>
<td width="60%">
Default data rate, in bps.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_DEVICE_FRIENDLY_NAME"></a><a id="scard_attr_device_friendly_name"></a><dl>
<dt><b>SCARD_ATTR_DEVICE_FRIENDLY_NAME</b></dt>
</dl>
</td>
<td width="60%">
Reader's display name.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_DEVICE_IN_USE"></a><a id="scard_attr_device_in_use"></a><dl>
<dt><b>SCARD_ATTR_DEVICE_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_DEVICE_SYSTEM_NAME"></a><a id="scard_attr_device_system_name"></a><dl>
<dt><b>SCARD_ATTR_DEVICE_SYSTEM_NAME</b></dt>
</dl>
</td>
<td width="60%">
Reader's system name.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_DEVICE_UNIT"></a><a id="scard_attr_device_unit"></a><dl>
<dt><b>SCARD_ATTR_DEVICE_UNIT</b></dt>
</dl>
</td>
<td width="60%">
Instance of this vendor's reader attached to the computer. The first instance will be device unit 0, the next will be unit 1 (if it is the same brand of reader) and so on. Two different brands of readers will both have zero for this value.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_ICC_INTERFACE_STATUS"></a><a id="scard_attr_icc_interface_status"></a><dl>
<dt><b>SCARD_ATTR_ICC_INTERFACE_STATUS</b></dt>
</dl>
</td>
<td width="60%">
Single byte. Zero if <a href="/windows/desktop/SecGloss/s-gly">smart card</a> electrical contact is not active; nonzero if contact is active.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_ICC_PRESENCE"></a><a id="scard_attr_icc_presence"></a><dl>
<dt><b>SCARD_ATTR_ICC_PRESENCE</b></dt>
</dl>
</td>
<td width="60%">
Single byte indicating smart card presence: 




0 = not present

1 = card present but not swallowed (applies only if reader supports smart card swallowing)

2 = card present (and swallowed if reader supports smart card swallowing)

4 = card confiscated.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_ICC_TYPE_PER_ATR"></a><a id="scard_attr_icc_type_per_atr"></a><dl>
<dt><b>SCARD_ATTR_ICC_TYPE_PER_ATR</b></dt>
</dl>
</td>
<td width="60%">
Single byte indicating smart card type: 




0 = unknown type

1 = 7816 Asynchronous

2 = 7816 Synchronous

Other values RFU.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_MAX_CLK"></a><a id="scard_attr_max_clk"></a><dl>
<dt><b>SCARD_ATTR_MAX_CLK</b></dt>
</dl>
</td>
<td width="60%">
Maximum clock rate, in kHz.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_MAX_DATA_RATE"></a><a id="scard_attr_max_data_rate"></a><dl>
<dt><b>SCARD_ATTR_MAX_DATA_RATE</b></dt>
</dl>
</td>
<td width="60%">
Maximum data rate, in bps.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_MAX_IFSD"></a><a id="scard_attr_max_ifsd"></a><dl>
<dt><b>SCARD_ATTR_MAX_IFSD</b></dt>
</dl>
</td>
<td width="60%">
Maximum bytes for information file size device.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_POWER_MGMT_SUPPORT"></a><a id="scard_attr_power_mgmt_support"></a><dl>
<dt><b>SCARD_ATTR_POWER_MGMT_SUPPORT</b></dt>
</dl>
</td>
<td width="60%">
Zero if device does not support power down while smart card is inserted. Nonzero otherwise.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_PROTOCOL_TYPES"></a><a id="scard_attr_protocol_types"></a><dl>
<dt><b>SCARD_ATTR_PROTOCOL_TYPES</b></dt>
</dl>
</td>
<td width="60%">
<b>DWORD</b> encoded as 0x0<i>rrrpppp</i> where <i>rrr</i> is RFU and should be 0x000. <i>pppp</i> encodes the supported protocol types. A '1' in a given bit position indicates support for the associated ISO protocol, so if bits zero and one are set, both <a href="/windows/desktop/SecGloss/t-gly">T=0</a> and <a href="/windows/desktop/SecGloss/t-gly">T=1</a> protocols are supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_VENDOR_IFD_SERIAL_NO"></a><a id="scard_attr_vendor_ifd_serial_no"></a><dl>
<dt><b>SCARD_ATTR_VENDOR_IFD_SERIAL_NO</b></dt>
</dl>
</td>
<td width="60%">
Vendor-supplied interface device serial number.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_VENDOR_IFD_TYPE"></a><a id="scard_attr_vendor_ifd_type"></a><dl>
<dt><b>SCARD_ATTR_VENDOR_IFD_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Vendor-supplied interface device type (model designation of reader).

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_VENDOR_IFD_VERSION"></a><a id="scard_attr_vendor_ifd_version"></a><dl>
<dt><b>SCARD_ATTR_VENDOR_IFD_VERSION</b></dt>
</dl>
</td>
<td width="60%">
Vendor-supplied interface device version (<b>DWORD</b> in the form 0x<i>MMmmbbbb</i> where <i>MM</i> = major version, <i>mm</i> = minor version, and <i>bbbb</i> = build number).

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_VENDOR_NAME"></a><a id="scard_attr_vendor_name"></a><dl>
<dt><b>SCARD_ATTR_VENDOR_NAME</b></dt>
</dl>
</td>
<td width="60%">
Vendor name.

</td>
</tr>
</table>

### -param pbAttr [out]

Pointer to a buffer that receives the attribute whose ID is supplied in <i>dwAttrId</i>. If this value is <b>NULL</b>, <b>SCardGetAttrib</b> ignores the buffer length supplied in <i>pcbAttrLen</i>, writes the length of the buffer that would have been returned if this parameter had not been <b>NULL</b> to <i>pcbAttrLen</i>, and returns a success code.

### -param pcbAttrLen [in, out]

Length of the <i>pbAttr</i> buffer in bytes, and receives the actual length of the received attribute If the buffer length is specified as SCARD_AUTOALLOCATE, then <i>pbAttr</i> is converted to a pointer to a byte pointer, and receives the address of a block of memory containing the attribute. This block of memory must be deallocated with 
<a href="/windows/desktop/api/winscard/nf-winscard-scardfreememory">SCardFreeMemory</a>.

## -returns

This function returns different values depending on whether it succeeds or fails.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Success</b></dt>
</dl>
</td>
<td width="60%">
SCARD_S_SUCCESS.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Attribute value not supported.</b></dt>
</dl>
</td>
<td width="60%">
ERROR_NOT_SUPPORTED.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other Failure</b></dt>
</dl>
</td>
<td width="60%">
An error code. For more information, see 
<a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.

</td>
</tr>
</table>

## -remarks

The <b>SCardGetAttrib</b> function is a direct card access function. For more information on other direct access functions, see 
<a href="/windows/desktop/SecAuthN/direct-card-access-functions">Direct Card Access Functions</a>.


#### Examples

The following example shows how to retrieve an attribute for a card reader. The example assumes that hCardHandle is a valid handle obtained from a previous call to the <a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a> function.


```cpp
LPBYTE   pbAttr = NULL;
DWORD    cByte = SCARD_AUTOALLOCATE;
DWORD    i;
LONG     lReturn;

lReturn = SCardGetAttrib(hCardHandle,
                         SCARD_ATTR_VENDOR_NAME,
                         (LPBYTE)&pbAttr,
                         &cByte);
if ( SCARD_S_SUCCESS != lReturn )
{
    if ( ERROR_NOT_SUPPORTED == lReturn )
        printf("Value not supported\n");
    else
    {
        // Some other error occurred.
        printf("Failed SCardGetAttrib - %x\n", lReturn);
        exit(1);  // Or other appropriate action
    }
}
else
{
    // Output the bytes.
    for (i = 0; i < cByte; i++)
        printf("%c", *(pbAttr+i));
    printf("\n");

    // Free the memory when done.
    // hContext was set earlier by SCardEstablishContext
    lReturn = SCardFreeMemory( hContext, pbAttr );
}

```

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardfreememory">SCardFreeMemory</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardsetattrib">SCardSetAttrib</a>