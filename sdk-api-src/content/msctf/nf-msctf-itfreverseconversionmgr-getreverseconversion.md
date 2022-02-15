---
UID: NF:msctf.ITfReverseConversionMgr.GetReverseConversion
title: ITfReverseConversionMgr::GetReverseConversion (msctf.h)
description: Retrieves an ITfReverseConversion object that can perform reverse conversions.
helpviewer_keywords: ["GetReverseConversion","GetReverseConversion method [Text Services Framework]","GetReverseConversion method [Text Services Framework]","ITfReverseConversionMgr interface","ITfReverseConversionMgr interface [Text Services Framework]","GetReverseConversion method","ITfReverseConversionMgr.GetReverseConversion","ITfReverseConversionMgr::GetReverseConversion","TF_RCM_COMLESS","TF_RCM_HINT_COLLISION","TF_RCM_HINT_READING_LENGTH","TF_RCM_VKEY","msctf/ITfReverseConversionMgr::GetReverseConversion","tsf.itfreverseconversionmgr_getreverseconversion"]
old-location: tsf\itfreverseconversionmgr_getreverseconversion.htm
tech.root: TSF
ms.assetid: 959bd98f-5b97-4bb8-a62d-9adfada25746
ms.date: 12/05/2018
ms.keywords: GetReverseConversion, GetReverseConversion method [Text Services Framework], GetReverseConversion method [Text Services Framework],ITfReverseConversionMgr interface, ITfReverseConversionMgr interface [Text Services Framework],GetReverseConversion method, ITfReverseConversionMgr.GetReverseConversion, ITfReverseConversionMgr::GetReverseConversion, TF_RCM_COMLESS, TF_RCM_HINT_COLLISION, TF_RCM_HINT_READING_LENGTH, TF_RCM_VKEY, msctf/ITfReverseConversionMgr::GetReverseConversion, tsf.itfreverseconversionmgr_getreverseconversion
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 with SP1 [desktop apps only]
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfReverseConversionMgr::GetReverseConversion
 - msctf/ITfReverseConversionMgr::GetReverseConversion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfReverseConversionMgr.GetReverseConversion
---

# ITfReverseConversionMgr::GetReverseConversion


## -description

<p class="CCE_Message">[<b>GetReverseConversion</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For internal use only.]

Retrieves an <a href="/windows/desktop/api/msctf/nn-msctf-itfreverseconversion">ITfReverseConversion</a> object that can perform reverse conversions.

## -parameters

### -param langid [in]

 The language ID of the profile to which the target strings belong.

### -param guidProfile [in]

 The GUID of the profile to which the target strings belong.

### -param dwflag [in]

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_RCM_COMLESS"></a><a id="tf_rcm_comless"></a><dl>
<dt><b>TF_RCM_COMLESS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Activate the reverse conversion interface without COM.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_RCM_VKEY"></a><a id="tf_rcm_vkey"></a><dl>
<dt><b>TF_RCM_VKEY</b></dt>
<dt> 0x00000002</dt>
</dl>
</td>
<td width="60%">
The output should be an array of virtual key codes (instead of character key codes). 

</td>
</tr>
<tr>
<td width="40%"><a id="TF_RCM_HINT_READING_LENGTH"></a><a id="tf_rcm_hint_reading_length"></a><dl>
<dt><b>TF_RCM_HINT_READING_LENGTH</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The reverse conversion should prioritize the order of entries in the output list based on the length of input sequence, with the shortest sequences first. It is possible that an input sequence with a low collision count might be much higher than an input sequence with a similar (but slightly higher) collision count. The interpretation of this flag varies depending on the IME. 

</td>
</tr>
<tr>
<td width="40%"><a id="TF_RCM_HINT_COLLISION_"></a><a id="tf_rcm_hint_collision_"></a><dl>
<dt><b>TF_RCM_HINT_COLLISION </b></dt>
<dt> 0x00000008</dt>
</dl>
</td>
<td width="60%">
The reverse conversion should prioritize the order of entries in the output list based on the collision count, with the entries containing the lowest number of collisions first.    If an input sequence corresponds to many more characters than a slightly longer input sequence, it might  be preferable to use the longer input sequence instead.  The IME determines whether this flag will affect the reverse conversion output.

</td>
</tr>
</table>

### -param ppReverseConversion [out]

 A pointer to the address of the ITfReverseConversion object that can perform the specified reverse conversion.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
An <a href="/windows/desktop/api/msctf/nn-msctf-itfreverseconversion">ITfReverseConversion</a> for the specified <i>langid</i> and <i>guidProfile</i> combination is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_NOTIMPL</dt>
</dl>
</td>
<td width="60%">
The specified <i>langid</i> and <i>guidProfile</i> combination does not support reverse conversion.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_FAIL</dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

A reverse conversion provides the keystroke sequences required to create the specified string.

When neither the <b>TF_RCM_HINT_COLLISION</b> or <b>TF_RCM_HINT_READING_LENGTH</b> flag is  specified for <i>dwflag</i>, the IME might not arrange the output in any sort of order.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfreverseconversionmgr">ITfReverseConversionMgr</a>