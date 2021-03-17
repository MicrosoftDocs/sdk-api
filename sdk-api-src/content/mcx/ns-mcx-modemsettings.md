---
UID: NS:mcx._MODEMSETTINGS
title: MODEMSETTINGS (mcx.h)
description: Contains information about a modem's configuration.
helpviewer_keywords: ["*LPMODEMSETTINGS","*PMODEMSETTINGS","LPMODEMSETTINGS","LPMODEMSETTINGS structure pointer","MDMSPKR_CALLSETUP","MDMSPKR_DIAL","MDMSPKR_OFF","MDMSPKR_ON","MDMVOL_HIGH","MDMVOL_LOW","MDMVOL_MEDIUM","MODEMSETTINGS","MODEMSETTINGS structure","PMODEMSETTINGS","PMODEMSETTINGS structure pointer","_win32_modemsettings_str","base.modemsettings_str","mcx/LPMODEMSETTINGS","mcx/MODEMSETTINGS","mcx/PMODEMSETTINGS"]
old-location: base\modemsettings_str.htm
tech.root: base
ms.assetid: 4648992b-eeeb-4a8d-8e08-7e80f0dc56ef
ms.date: 12/05/2018
ms.keywords: '*LPMODEMSETTINGS, *PMODEMSETTINGS, LPMODEMSETTINGS, LPMODEMSETTINGS structure pointer, MDMSPKR_CALLSETUP, MDMSPKR_DIAL, MDMSPKR_OFF, MDMSPKR_ON, MDMVOL_HIGH, MDMVOL_LOW, MDMVOL_MEDIUM, MODEMSETTINGS, MODEMSETTINGS structure, PMODEMSETTINGS, PMODEMSETTINGS structure pointer, _win32_modemsettings_str, base.modemsettings_str, mcx/LPMODEMSETTINGS, mcx/MODEMSETTINGS, mcx/PMODEMSETTINGS'
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
req.typenames: MODEMSETTINGS, *PMODEMSETTINGS, *LPMODEMSETTINGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MODEMSETTINGS
 - mcx/_MODEMSETTINGS
 - PMODEMSETTINGS
 - mcx/PMODEMSETTINGS
 - MODEMSETTINGS
 - mcx/MODEMSETTINGS
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
 - MODEMSETTINGS
---

# MODEMSETTINGS structure


## -description

Contains information about a modem's configuration.

## -struct-fields

### -field dwActualSize

The size of the data actually returned to the application, in bytes. This member may be less than the <b>dwRequiredSize</b> member if an application did not allocate enough space for the variable-length portion of the structure.

### -field dwRequiredSize

The number of bytes required for the entire 
<a href="/windows/desktop/api/mcx/ns-mcx-modemdevcaps">MODEMDEVCAPS</a> structure, including the variable-length portion.

### -field dwDevSpecificOffset

The offset of the provider-defined portion of the structure, in bytes relative to the beginning of the structure.

### -field dwDevSpecificSize

The size of the provider-defined portion of the structure, in bytes.

### -field dwCallSetupFailTimer

The maximum number of seconds the modem should wait, after dialing is completed, for an indication that a modem-to-modem connection has been established. If a connection is not established in this interval, the call is assumed to have failed. This member is equivalent to register S7 in Hayes® compatible modems.

### -field dwInactivityTimeout

The maximum number of seconds of inactivity allowed after a connection is established. If no data is either transmitted or received for this period of time, the call is automatically terminated. This time-out is used to avoid excessive long-distance charges or online service charges if an application unexpectedly locks up or the user leaves.

### -field dwSpeakerVolume

The volume level of the monitor speaker when the speaker is on. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MDMVOL_HIGH"></a><a id="mdmvol_high"></a><dl>
<dt><b>MDMVOL_HIGH</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
High volume.

</td>
</tr>
<tr>
<td width="40%"><a id="MDMVOL_LOW"></a><a id="mdmvol_low"></a><dl>
<dt><b>MDMVOL_LOW</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Low volume.

</td>
</tr>
<tr>
<td width="40%"><a id="MDMVOL_MEDIUM"></a><a id="mdmvol_medium"></a><dl>
<dt><b>MDMVOL_MEDIUM</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Medium volume.

</td>
</tr>
</table>
 

The 
<a href="/windows/desktop/api/mcx/ns-mcx-modemdevcaps">MODEMDEVCAPS</a> structure specifies the speaker volumes a modem supports. Actual volumes are hardware-specific.

### -field dwSpeakerMode

The speaker mode. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MDMSPKR_CALLSETUP"></a><a id="mdmspkr_callsetup"></a><dl>
<dt><b>MDMSPKR_CALLSETUP</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The speaker is on until a connection is established.

</td>
</tr>
<tr>
<td width="40%"><a id="MDMSPKR_DIAL"></a><a id="mdmspkr_dial"></a><dl>
<dt><b>MDMSPKR_DIAL</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The speaker is on until a connection is established, except that it is off while the modem is actually dialing.

</td>
</tr>
<tr>
<td width="40%"><a id="MDMSPKR_OFF"></a><a id="mdmspkr_off"></a><dl>
<dt><b>MDMSPKR_OFF</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The speaker is always off.

</td>
</tr>
<tr>
<td width="40%"><a id="MDMSPKR_ON"></a><a id="mdmspkr_on"></a><dl>
<dt><b>MDMSPKR_ON</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The speaker is always on.

</td>
</tr>
</table>

### -field dwPreferredModemOptions

The modem options requested by the application. The local and remote modems negotiate modem options during call setup; this member specifies the initial negotiating position of the local modem. 




The <b>dwModemOptions</b> member of the 
<a href="/windows/desktop/api/mcx/ns-mcx-modemdevcaps">MODEMDEVCAPS</a> structure specifies the modem options supported by the local modem. For a list of modem options, see the description of the 
<b>MODEMDEVCAPS</b> structure.

### -field dwNegotiatedModemOptions

The modem options that are actually in effect. This member is filled in after a connection is established and the local and remote modems negotiate modem options. 




The <b>dwModemOptions</b> member of the 
<a href="/windows/desktop/api/mcx/ns-mcx-modemdevcaps">MODEMDEVCAPS</a> structure specifies the modem options supported by the local modem. For a list of modem options, see the description of the 
<b>MODEMDEVCAPS</b> structure.

### -field dwNegotiatedDCERate

The DCE rate in effect. This member is filled in after a connection is established and the local and remote modems negotiate modem modulations.

### -field abVariablePortion

Optional provider-defined information.

## -see-also

<a href="/windows/desktop/api/mcx/ns-mcx-modemdevcaps">MODEMDEVCAPS</a>