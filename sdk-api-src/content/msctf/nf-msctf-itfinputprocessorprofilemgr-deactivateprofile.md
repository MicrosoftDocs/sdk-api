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

# ITfInputProcessorProfileMgr::DeactivateProfile


## -description


The <b>ITfInputProcessorProfileMgr::DeactivateProfile</b> method deactivates the specified text service's profile or keyboard layout.


## -parameters




### -param dwProfileType [in]

[in] The type of this profile. This is one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_PROFILETYPE_INPUTPROCESSOR"></a><a id="tf_profiletype_inputprocessor"></a><dl>
<dt><b>TF_PROFILETYPE_INPUTPROCESSOR</b></dt>
</dl>
</td>
<td width="60%">
This is a text service.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_PROFILETYPE_KEYBOARDLAYOUT"></a><a id="tf_profiletype_keyboardlayout"></a><dl>
<dt><b>TF_PROFILETYPE_KEYBOARDLAYOUT</b></dt>
</dl>
</td>
<td width="60%">
This is a keyboard layout.

</td>
</tr>
</table>
 


### -param langid [in]

[in] The language id of the profile to be activated.


### -param clsid [in]

[in] The CLSID of the text service of the profile to be activated. This must be CLSID_NULL if <i>dwProfileType</i> is TF_PROFILETYPE_KEYBOARDLAYOUT.


### -param guidProfile [in]

[in] The guidProfile of the profile to be activated. This must be GUID_NULL if <i>dwProfileType</i> is TF_PROFILETYPE_KEYBOARDLAYOUT.


### -param hkl [in]

[in] The handle of the keyboard layout. This must be <b>NULL</b> if <i>dwProfileType</i> is TF_PROFILETYPE_INPUTPROCESSOR.


### -param dwFlags [in]

The combination of the following bits:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_IPPMF_FORPROCESS"></a><a id="tf_ippmf_forprocess"></a><dl>
<dt><b>TF_IPPMF_FORPROCESS</b></dt>
</dl>
</td>
<td width="60%">
Deactivate this profile for all threads in the process.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IPPMF_FORSESSION"></a><a id="tf_ippmf_forsession"></a><dl>
<dt><b>TF_IPPMF_FORSESSION</b></dt>
</dl>
</td>
<td width="60%">
Deactivate this profile for all threads in the current desktop.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IPPMF_DISABLEPROFILE"></a><a id="tf_ippmf_disableprofile"></a><dl>
<dt><b>TF_IPPMF_DISABLEPROFILE</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d60bb748-3c61-466d-9c17-df7bc4904994">ITfInputProcessorProfileMgr</a>



<a href="https://msdn.microsoft.com/5e5b3f26-332a-456e-875f-12e440ae67ba">ITfInputProcessorProfileMgr::ActivateProfile
      </a>
 

 

