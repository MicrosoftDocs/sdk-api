---
UID: NS:mcx._MODEMDEVCAPS
title: MODEMDEVCAPS (mcx.h)
description: Contains information about the capabilities of a modem.
helpviewer_keywords: ["*LPMODEMDEVCAPS","*PMODEMDEVCAPS","DIALOPTION_BILLING","DIALOPTION_DIALTONE","DIALOPTION_QUIET","LPMODEMDEVCAPS","LPMODEMDEVCAPS structure pointer","MDMSPKRFLAG_CALLSETUP","MDMSPKRFLAG_DIAL","MDMSPKRFLAG_OFF","MDMSPKRFLAG_ON","MDMVOLFLAG_HIGH","MDMVOLFLAG_LOW","MDMVOLFLAG_MEDIUM","MDM_BLIND_DIAL","MDM_CCITT_OVERRIDE","MDM_CELLULAR","MDM_COMPRESSION","MDM_DIAGNOSTICS","MDM_ERROR_CONTROL","MDM_FLOWCONTROL_HARD","MDM_FLOWCONTROL_SOFT","MDM_FORCED_EC","MDM_SPEED_ADJUST","MDM_TONE_DIAL","MDM_V23_OVERRIDE","MODEMDEVCAPS","MODEMDEVCAPS structure","PMODEMDEVCAPS","PMODEMDEVCAPS structure pointer","_win32_modemdevcaps_str","base.modemdevcaps_str","mcx/LPMODEMDEVCAPS","mcx/MODEMDEVCAPS","mcx/PMODEMDEVCAPS"]
old-location: base\modemdevcaps_str.htm
tech.root: base
ms.assetid: 7e9e37c7-416d-4550-87e3-7412cff9a49e
ms.date: 12/05/2018
ms.keywords: '*LPMODEMDEVCAPS, *PMODEMDEVCAPS, DIALOPTION_BILLING, DIALOPTION_DIALTONE, DIALOPTION_QUIET, LPMODEMDEVCAPS, LPMODEMDEVCAPS structure pointer, MDMSPKRFLAG_CALLSETUP, MDMSPKRFLAG_DIAL, MDMSPKRFLAG_OFF, MDMSPKRFLAG_ON, MDMVOLFLAG_HIGH, MDMVOLFLAG_LOW, MDMVOLFLAG_MEDIUM, MDM_BLIND_DIAL, MDM_CCITT_OVERRIDE, MDM_CELLULAR, MDM_COMPRESSION, MDM_DIAGNOSTICS, MDM_ERROR_CONTROL, MDM_FLOWCONTROL_HARD, MDM_FLOWCONTROL_SOFT, MDM_FORCED_EC, MDM_SPEED_ADJUST, MDM_TONE_DIAL, MDM_V23_OVERRIDE, MODEMDEVCAPS, MODEMDEVCAPS structure, PMODEMDEVCAPS, PMODEMDEVCAPS structure pointer, _win32_modemdevcaps_str, base.modemdevcaps_str, mcx/LPMODEMDEVCAPS, mcx/MODEMDEVCAPS, mcx/PMODEMDEVCAPS'
req.header: mcx.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MODEMDEVCAPS, *PMODEMDEVCAPS, *LPMODEMDEVCAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MODEMDEVCAPS
 - mcx/_MODEMDEVCAPS
 - PMODEMDEVCAPS
 - mcx/PMODEMDEVCAPS
 - MODEMDEVCAPS
 - mcx/MODEMDEVCAPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mcx.h
api_name:
 - MODEMDEVCAPS
---

# MODEMDEVCAPS structure


## -description

Contains information about the capabilities of a modem.

## -struct-fields

### -field dwActualSize

The size of the data actually returned to the application, in bytes. This member may be less than the <b>dwRequiredSize</b> member, if an application did not allocate enough space for the variable-length portion of the structure.

### -field dwRequiredSize

The number of bytes required for the entire 
<b>MODEMDEVCAPS</b> structure, including the variable-length portion.

### -field dwDevSpecificOffset

The offset of the provider-defined portion of the structure, in bytes relative to the beginning of the structure.

### -field dwDevSpecificSize

The size of the provider-defined portion of the structure, in bytes.

### -field dwModemProviderVersion

The version of the service provider. The format and use of this member depends on the service provider.

### -field dwModemManufacturerOffset

The offset of a text string that contains the name of the modem manufacturer, in bytes relative to the beginning of the structure.

### -field dwModemManufacturerSize

The length of the modem manufacturer name, in bytes. The string is not null-terminated.

### -field dwModemModelOffset

The offset of a text string that contains the model of the modem, in bytes relative to the beginning of the structure.

### -field dwModemModelSize

The length of the model name, in bytes. The string is not null-terminated.

### -field dwModemVersionOffset

The offset of a text string that gives the version and revision of the attached modem, if the provider could determine the information. The offset is specified in bytes relative to the beginning of the structure.

### -field dwModemVersionSize

The length of the modem version string, in bytes. The string is not null-terminated.

### -field dwDialOptions

The dialing options supported by the modem device. This member can be zero or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DIALOPTION_BILLING"></a><a id="dialoption_billing"></a><dl>
<dt><b>DIALOPTION_BILLING</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The modem supports waiting for billing tone (bong).

</td>
</tr>
<tr>
<td width="40%"><a id="DIALOPTION_DIALTONE"></a><a id="dialoption_dialtone"></a><dl>
<dt><b>DIALOPTION_DIALTONE</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The modem supports waiting for a dial tone.

</td>
</tr>
<tr>
<td width="40%"><a id="DIALOPTION_QUIET"></a><a id="dialoption_quiet"></a><dl>
<dt><b>DIALOPTION_QUIET</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
The modem supports waiting for quiet.

</td>
</tr>
</table>

### -field dwCallSetupFailTimer

The maximum call setup timeout supported by the modem, in seconds. This is the largest value that can be specified for the corresponding member of the 
<a href="/windows/desktop/api/mcx/ns-mcx-modemsettings">MODEMSETTINGS</a> structure.

### -field dwInactivityTimeout

The maximum inactivity timeout supported by the modem, in tenths of seconds. This is the largest value that can be specified for the corresponding member of the 
<a href="/windows/desktop/api/mcx/ns-mcx-modemsettings">MODEMSETTINGS</a> structure.

### -field dwSpeakerVolume

The speaker volume settings supported by the modem. This member can be zero or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MDMVOLFLAG_HIGH"></a><a id="mdmvolflag_high"></a><dl>
<dt><b>MDMVOLFLAG_HIGH</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The modem supports high (MDMVOL_HIGH) volume.

</td>
</tr>
<tr>
<td width="40%"><a id="MDMVOLFLAG_LOW"></a><a id="mdmvolflag_low"></a><dl>
<dt><b>MDMVOLFLAG_LOW</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The modem supports low (MDMVOL_LOW) volume.

</td>
</tr>
<tr>
<td width="40%"><a id="MDMVOLFLAG_MEDIUM"></a><a id="mdmvolflag_medium"></a><dl>
<dt><b>MDMVOLFLAG_MEDIUM</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The modem supports medium (MDMVOL_MEDIUM) volume.

</td>
</tr>
</table>

### -field dwSpeakerMode

The speaker mode settings supported by the modem. This member can be zero or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MDMSPKRFLAG_CALLSETUP"></a><a id="mdmspkrflag_callsetup"></a><dl>
<dt><b>MDMSPKRFLAG_CALLSETUP</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The modem supports the MDMSPKR_CALLSETUP speaker mode.

</td>
</tr>
<tr>
<td width="40%"><a id="MDMSPKRFLAG_DIAL"></a><a id="mdmspkrflag_dial"></a><dl>
<dt><b>MDMSPKRFLAG_DIAL</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The modem supports the MDMSPKR_DIAL speaker mode.

</td>
</tr>
<tr>
<td width="40%"><a id="MDMSPKRFLAG_OFF"></a><a id="mdmspkrflag_off"></a><dl>
<dt><b>MDMSPKRFLAG_OFF</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The modem supports the MDMSPKR_OFF speaker mode.

</td>
</tr>
<tr>
<td width="40%"><a id="MDMSPKRFLAG_ON"></a><a id="mdmspkrflag_on"></a><dl>
<dt><b>MDMSPKRFLAG_ON</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The modem supports the MDMSPKR_ON speaker mode.

</td>
</tr>
</table>

### -field dwModemOptions

The modem options. This member can be zero or more of the following values.



#### MDM_BLIND_DIAL (0x00000200)



#### MDM_CCITT_OVERRIDE (0x00000040)



#### MDM_CELLULAR (0x00000008)



#### MDM_COMPRESSION (0x00000001)



#### MDM_DIAGNOSTICS (0x000000800)



#### MDM_ERROR_CONTROL (0x00000002)



#### MDM_FLOWCONTROL_HARD (0x00000010)



#### MDM_FLOWCONTROL_SOFT (0x00000020)



#### MDM_FORCED_EC (0x00000004)



#### MDM_SPEED_ADJUST (0x00000080)



#### MDM_TONE_DIAL (0x00000100)



#### MDM_V23_OVERRIDE (0x00000400)


When 
<b>MODEMDEVCAPS</b> is used to set modem options, as part of the 
<a href="/windows/desktop/api/mcx/ns-mcx-modemsettings">MODEMSETTINGS</a> structure, these values are used as follows.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MDM_CCITT_OVERRIDE"></a><a id="mdm_ccitt_override"></a><dl>
<dt><b>MDM_CCITT_OVERRIDE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
When set, CCITT modulations are enabled for V.21 and V.22 or V.23. 




When clear, bell modulations are enabled for 103 and 212A.

</td>
</tr>
<tr>
<td width="40%"><a id="MDM_V23_OVERRIDE"></a><a id="mdm_v23_override"></a><dl>
<dt><b>MDM_V23_OVERRIDE</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
When set, CCITT modulations are enabled for V.23. 




When clear, CCITT modulations are enabled for V.21 and V.22.

</td>
</tr>
</table>
 

For V.23 to be set, both MDM_CCITT_OVERRIDE and MDM_V23_OVERRIDE must be set.

### -field dwMaxDTERate

The maximum DTE rate in bits per second.

### -field dwMaxDCERate

The maximum DCE rate in bits per second.

### -field abVariablePortion

Variable-length information, including strings and any provider-defined information.

## -see-also

<a href="/windows/desktop/api/mcx/ns-mcx-modemsettings">MODEMSETTINGS</a>