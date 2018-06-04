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

# ITfFnConfigureRegisterWord::Show


## -description




## -parameters




### -param hwndParent [in]

Handle of the parent window. The text service typically uses this as the parent or owner window when creating the dialog box.


### -param langid [in]

Contains a <b>LANGID</b> that specifies the identifier of the language currently used by the Input Method Editor (IME).


### -param rguidProfile [in]

Contains a GUID that specifies the language profile identifier that the text service is under. This is the value specified in <a href="https://msdn.microsoft.com/d132bff1-24de-4e43-859b-2425ba7de8f0">ITfInputProcessorProfiles::AddLanguageProfile</a> when the profile was added.


### -param bstrRegistered [in]

Contains a <b>BSTR</b> that contains the word to be registered with the text service. This is optional and can be NULL. If NULL, the text service should display a default register word dialog box.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The text service does not implement this method.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/515e5f01-a68f-4e67-acf5-cac1923d485e">ITfFnConfigureRegisterWord</a>



<a href="https://msdn.microsoft.com/d132bff1-24de-4e43-859b-2425ba7de8f0">ITfInputProcessorProfiles::AddLanguageProfile
      </a>
 

 

