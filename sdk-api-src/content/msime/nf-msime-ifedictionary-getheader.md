---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IFEDictionary::GetHeader


## -description


Gets a dictionary header from a dictionary file without opening the dictionary.


## -parameters




### -param pchDictPath [in, out, optional]

A <b>NULL</b>-terminated string containing the path and name of the dictionary file.


### -param pshf [out]

The <a href="https://msdn.microsoft.com/CFFEFEDC-F614-4DD4-B1A1-4D236339E817">IMESHF</a> header of the file. Can be <b>NULL</b>.


### -param pjfmt [out]

The dictionary format. This can be one of the following values:

<a id="IFED_UNKNOWN"></a>
<a id="ifed_unknown"></a>


#### IFED_UNKNOWN

<a id="IFED_MSIME2_BIN_SYSTEM"></a>
<a id="ifed_msime2_bin_system"></a>


#### IFED_MSIME2_BIN_SYSTEM

<a id="IFED_MSIME2_BIN_USER"></a>
<a id="ifed_msime2_bin_user"></a>


#### IFED_MSIME2_BIN_USER

<a id="IFED_MSIME2_TEXT_USER"></a>
<a id="ifed_msime2_text_user"></a>


#### IFED_MSIME2_TEXT_USER

<a id="IFED_MSIME95_BIN_SYSTEM"></a>
<a id="ifed_msime95_bin_system"></a>


#### IFED_MSIME95_BIN_SYSTEM

<a id="IFED_MSIME95_BIN_USER"></a>
<a id="ifed_msime95_bin_user"></a>


#### IFED_MSIME95_BIN_USER

<a id="IFED_MSIME95_TEXT_USER"></a>
<a id="ifed_msime95_text_user"></a>


#### IFED_MSIME95_TEXT_USER

<a id="IFED_MSIME97_BIN_SYSTEM"></a>
<a id="ifed_msime97_bin_system"></a>


#### IFED_MSIME97_BIN_SYSTEM

<a id="IFED_MSIME97_BIN_USER"></a>
<a id="ifed_msime97_bin_user"></a>


#### IFED_MSIME97_BIN_USER

<a id="IFED_MSIME97_TEXT_USER"></a>
<a id="ifed_msime97_text_user"></a>


#### IFED_MSIME97_TEXT_USER

<a id="IFED_MSIME98_BIN_SYSTEM"></a>
<a id="ifed_msime98_bin_system"></a>


#### IFED_MSIME98_BIN_SYSTEM

<a id="IFED_MSIME98_BIN_USER"></a>
<a id="ifed_msime98_bin_user"></a>


#### IFED_MSIME98_BIN_USER

<a id="IFED_MSIME98_TEST_USER"></a>
<a id="ifed_msime98_test_user"></a>


#### IFED_MSIME98_TEST_USER

<a id="IFED_ACTIVE_DICT"></a>
<a id="ifed_active_dict"></a>


#### IFED_ACTIVE_DICT

<a id="IFED_ATOK9"></a>
<a id="ifed_atok9"></a>


#### IFED_ATOK9

<a id="IFED_ATOK10"></a>
<a id="ifed_atok10"></a>


#### IFED_ATOK10

<a id="IFED_NEC_AI_"></a>
<a id="ifed_nec_ai_"></a>


#### IFED_NEC_AI_

<a id="IFED_WX_II"></a>
<a id="ifed_wx_ii"></a>


#### IFED_WX_II

<a id="IFED_WX_III"></a>
<a id="ifed_wx_iii"></a>


#### IFED_WX_III

<a id="IFED_VJE_20"></a>
<a id="ifed_vje_20"></a>


#### IFED_VJE_20

<a id="IFED_MSIME98_SYSTEM_CE"></a>
<a id="ifed_msime98_system_ce"></a>


#### IFED_MSIME98_SYSTEM_CE

<a id="IFED_MSIME_BIN_SYSTEM"></a>
<a id="ifed_msime_bin_system"></a>


#### IFED_MSIME_BIN_SYSTEM

<a id="IFED_MSIME_BIN_USER"></a>
<a id="ifed_msime_bin_user"></a>


#### IFED_MSIME_BIN_USER

<a id="IFED_MSIME_TEXT_USER"></a>
<a id="ifed_msime_text_user"></a>


#### IFED_MSIME_TEXT_USER

<a id="IFED_PIME2_BIN_USER"></a>
<a id="ifed_pime2_bin_user"></a>


#### IFED_PIME2_BIN_USER

<a id="IFED_PIME2_BIN_SYSTEM"></a>
<a id="ifed_pime2_bin_system"></a>


#### IFED_PIME2_BIN_SYSTEM

<a id="IFED_PIME2_BIN_STANDARD_SYSTEM"></a>
<a id="ifed_pime2_bin_standard_system"></a>


#### IFED_PIME2_BIN_STANDARD_SYSTEM


### -param pulType [out]

The dictionary type. This is a combination of one or more of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IFED_TYPE_NONE"></a><a id="ifed_type_none"></a><dl>
<dt><b>IFED_TYPE_NONE</b></dt>
</dl>
</td>
<td width="60%">
Undefined.

</td>
</tr>
<tr>
<td width="40%"><a id="IFED_TYPE_GENERAL"></a><a id="ifed_type_general"></a><dl>
<dt><b>IFED_TYPE_GENERAL</b></dt>
</dl>
</td>
<td width="60%">
General dictionary.

</td>
</tr>
<tr>
<td width="40%"><a id="IFED_TYPE_NAMEPLACE"></a><a id="ifed_type_nameplace"></a><dl>
<dt><b>IFED_TYPE_NAMEPLACE</b></dt>
</dl>
</td>
<td width="60%">
Name/place dictionary.

</td>
</tr>
<tr>
<td width="40%"><a id="IFED_TYPE_SPEECH"></a><a id="ifed_type_speech"></a><dl>
<dt><b>IFED_TYPE_SPEECH</b></dt>
</dl>
</td>
<td width="60%">
Speech dictionary.

</td>
</tr>
<tr>
<td width="40%"><a id="IFED_TYPE_REVERSE"></a><a id="ifed_type_reverse"></a><dl>
<dt><b>IFED_TYPE_REVERSE</b></dt>
</dl>
</td>
<td width="60%">
Reverse dictionary.

</td>
</tr>
<tr>
<td width="40%"><a id="IFED_TYPE_ENGLISH"></a><a id="ifed_type_english"></a><dl>
<dt><b>IFED_TYPE_ENGLISH</b></dt>
</dl>
</td>
<td width="60%">
English dictionary.

</td>
</tr>
<tr>
<td width="40%"><a id="IFED_TYPE_ALL"></a><a id="ifed_type_all"></a><dl>
<dt><b>IFED_TYPE_ALL</b></dt>
</dl>
</td>
<td width="60%">
All of the above types.

</td>
</tr>
</table>
 


## -returns



One of the following:

<ul>
<li><b>S_OK</b></li>
<li><b>IFED_E_INVALID_FORMAT</b></li>
<li><b>E_FAIL</b></li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/4C63FF43-0170-4038-AB01-72441E1BB189">IFEDictionary</a>



<a href="https://msdn.microsoft.com/CFFEFEDC-F614-4DD4-B1A1-4D236339E817">IMESHF</a>
 

 

