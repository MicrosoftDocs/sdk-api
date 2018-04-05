---
UID: NF:msctf.ITfInputProcessorProfileMgr.GetActiveProfile
title: ITfInputProcessorProfileMgr::GetActiveProfile method
author: windows-driver-content
description: This method returns the current active profile.
old-location: tsf\itfinputprocessorprofilemgr_getactiveprofile.htm
old-project: TSF
ms.assetid: 4fd03327-c0c4-4dd6-b68a-8faae48c9a3d
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetActiveProfile method [Text Services Framework], GetActiveProfile method [Text Services Framework], ITfInputProcessorProfileMgr interface, GetActiveProfile,ITfInputProcessorProfileMgr.GetActiveProfile, ITfInputProcessorProfileMgr, ITfInputProcessorProfileMgr interface [Text Services Framework], GetActiveProfile method, ITfInputProcessorProfileMgr::GetActiveProfile, msctf/ITfInputProcessorProfileMgr::GetActiveProfile, tsf.itfinputprocessorprofilemgr_getactiveprofile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfInputProcessorProfileMgr.GetActiveProfile
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfInputProcessorProfileMgr::GetActiveProfile method


## -description


This method returns the current active profile.


## -parameters




### -param catid [in]

[in] The category id for the profile. This must be GUID_TFCAT_TIP_KEYBOARD. Only GUID_TFCAT_TIP_KEYBOARD is supported.


### -param pProfile [out]

[out] The buffer to receive the profile information.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The profile was not found or is not active.

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
 



