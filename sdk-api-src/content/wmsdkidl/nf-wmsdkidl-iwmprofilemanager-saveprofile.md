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

# IWMProfileManager::SaveProfile


## -description



The <b>SaveProfile</b> method saves a profile into an XML-formatted string.




## -parameters




### -param pIWMProfile




### -param pwszProfile [in]

Pointer to a wide-character <b>null</b>-terminated string containing the profile. Set this to <b>NULL</b> to retrieve the length of string required.


### -param pdwLength [in, out]

On input, specifies the length of the <i>pwszProfile</i> string. On output, if the method succeeds, specifies a pointer to a <b>DWORD</b> containing the number of characters, including the terminating <b>null</b> character, required to hold the profile.


#### - pProfile [in]

Pointer to the <a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile</a> interface of the object containing the profile data to be saved.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Either the <i>pIWMProfile</i> or <i>pdwLength</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



You should make two calls to <b>SaveProfile</b>. On the first call, pass <b>NULL</b> as <i>pwszProfile</i>. On return, the value of <i>pdwLength</i> is set to the length required to hold the profile in string form. Then you can allocate the required amount of memory for the buffer and pass a pointer to it as <i>pwszProfile</i> on the second call.

This string contains all the profile information. It must not be displayed to users, and should not be altered. To change the settings in a saved profile, load it using the profile manager and change the settings using the profile object and related objects.

To save a custom profile for later use, you must save the content of the returned string in a .prx file. For more information on .prx files, see <a href="https://msdn.microsoft.com/library/windows/hardware/mt764032">Profiles</a>.

To load a saved custom profile, copy the contents of the profile from the .prx file to a string and use <a href="https://msdn.microsoft.com/c645b6cc-e10d-4335-91c4-8bfd430ca76b">IWMProfileManager::LoadProfileByData</a>.




## -see-also




<a href="https://msdn.microsoft.com/e5ec945c-4513-48ad-8bef-e0fb54826991">IWMProfileManager Interface</a>
 

 

