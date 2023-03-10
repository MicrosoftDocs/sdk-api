---
UID: NS:msctf.TF_INPUTPROCESSORPROFILE
title: TF_INPUTPROCESSORPROFILE (msctf.h)
description: This structure contains data for the input processor profile.
helpviewer_keywords: ["TF_INPUTPROCESSORPROFILE","TF_INPUTPROCESSORPROFILE structure [Text Services Framework]","_tsf_tf_inputprocessorprofile_ref","msctf/TF_INPUTPROCESSORPROFILE","tsf.tf_inputprocessorprofile"]
old-location: tsf\tf_inputprocessorprofile.htm
tech.root: TSF
ms.assetid: fecaf8f5-1323-4a2e-94ee-26b5712ed643
ms.date: 12/05/2018
ms.keywords: TF_INPUTPROCESSORPROFILE, TF_INPUTPROCESSORPROFILE structure [Text Services Framework], _tsf_tf_inputprocessorprofile_ref, msctf/TF_INPUTPROCESSORPROFILE, tsf.tf_inputprocessorprofile
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TF_INPUTPROCESSORPROFILE
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TF_INPUTPROCESSORPROFILE
 - msctf/TF_INPUTPROCESSORPROFILE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msctf.h
api_name:
 - TF_INPUTPROCESSORPROFILE
---

# TF_INPUTPROCESSORPROFILE structure


## -description

This structure contains data for the input processor profile.

## -struct-fields

### -field dwProfileType

The type of this profile. This is one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>TF_PROFILETYPE_INPUTPROCESSOR</td>
<td>This is a text service.</td>
</tr>
<tr>
<td>TF_PROFILETYPE_KEYBOARDLAYOUT</td>
<td>This is a keyboard layout.</td>
</tr>
</table>

### -field langid

The language id for this profile.

### -field clsid

The CLSID of the text service. This is CLSID_NULL if this profile is a keyboard layout.

### -field guidProfile

The guidProfile of the text services. This is GUID_NULL if this profile is a keyboard layout.

### -field catid

The category of this text service. This category is GUID_TFCAT_TIP_KEYBOARD, GUID_TFCAT_TIP_SPEECH, GUID_TFCAT_TIP_HANDWRITING or something in GUID_TFCAT_CATEGORY_OF_TIP.

### -field hklSubstitute

The keyboard layout handle of the substitute for this text service. This can be <b>NULL</b> if the text service does not have a substitute or this profile is a keyboard layout.

### -field dwCaps

The flag to specify the capability of text service. This is the combination of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>TF_IPP_CAPS_DISABLEONTRANSITORY</td>
<td>This text service profile is disabled on transitory context.</td>
</tr>
<tr>
<td>TF_IPP_CAPS_SECUREMODESUPPORT</td>
<td>This text service supports the secure mode. This is categorized in GUID_TFCAT_TIPCAP_SECUREMODE.</td>
</tr>
<tr>
<td>TF_IPP_CAPS_UIELEMENTENABLED</td>
<td>This text service supports the UIElement. This is categorized in GUID_TFCAT_TIPCAP_UIELEMENTENABLED.</td>
</tr>
<tr>
<td>TF_IPP_CAPS_COMLESSSUPPORT</td>
<td>This text service can be activated without COM. This is categorized in GUID_TFCAT_TIPCAP_COMLESS.</td>
</tr>
<tr>
<td>TF_IPP_CAPS_WOW16SUPPORT</td>
<td>This text service can be activated on 16bit task. This is categorized in GUID_TFCAT_TIPCAP_WOW16.</td>
</tr>
<tr>
<td>TF_IPP_CAPS_IMMERSIVESUPPORT</td>
<td><b>Starting with Windows 8:</b> This text service has been tested to run properly in a Windows Store app.</td>
</tr>
<tr>
<td>TF_IPP_CAPS_SYSTRAYSUPPORT</td>
<td><b>Starting with Windows 8:</b> This text service supports inclusion in the System Tray.  This is used for text services that do not set the TF_IPP_CAPS_IMMERSIVESUPPORT flag but  are still compatible with the System Tray.</td>
</tr>
</table>

### -field hkl

The keyboard layout handle. This is <b>NULL</b> if this profile is a text service.

### -field dwFlags

The flag for this profile. This is a combination of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>TF_IPP_FLAG_ACTIVE</td>
<td>This profile is now active.</td>
</tr>
<tr>
<td>TF_IPP_FLAG_ENABLED</td>
<td>This profile is enabled.</td>
</tr>
<tr>
<td>TF_IPP_FLAG_SUBSTITUTEDBYINPUTPROCESSOR</td>
<td>This profile is substituted by a text service.</td>
</tr>
</table>

