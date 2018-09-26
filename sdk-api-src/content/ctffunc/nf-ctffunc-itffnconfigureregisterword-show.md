---
UID: NF:ctffunc.ITfFnConfigureRegisterWord.Show
title: ITfFnConfigureRegisterWord::Show
author: windows-sdk-content
description: ITfFnConfigureRegisterWord::Show method
old-location: tsf\itffnconfigureregisterword_show.htm
tech.root: TSF
ms.assetid: 61eb7452-2ada-4832-bd16-87ac56fedc6d
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITfFnConfigureRegisterWord interface [Text Services Framework],Show method, ITfFnConfigureRegisterWord.Show, ITfFnConfigureRegisterWord::Show, Show, Show method [Text Services Framework], Show method [Text Services Framework],ITfFnConfigureRegisterWord interface, _tsf_itffnconfigureregisterword_show_ref, ctffunc/ITfFnConfigureRegisterWord::Show, tsf.itffnconfigureregisterword_show
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Imekrcic.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imekrcic.dll
api_name:
 - ITfFnConfigureRegisterWord.Show
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfFnConfigureRegisterWord::Show


## -description




## -parameters




### -param hwndParent [in]

Handle of the parent window. The text service typically uses this as the parent or owner window when creating the dialog box.


### -param langid [in]

Contains a <b>LANGID</b> that specifies the identifier of the language currently used by the Input Method Editor (IME).


### -param rguidProfile [in]

Contains a GUID that specifies the language profile identifier that the text service is under. This is the value specified in <a href="https://msdn.microsoft.com/en-us/library/ms628545(v=VS.85).aspx">ITfInputProcessorProfiles::AddLanguageProfile</a> when the profile was added.


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




<a href="https://msdn.microsoft.com/en-us/library/ms538926(v=VS.85).aspx">ITfFnConfigureRegisterWord</a>



<a href="https://msdn.microsoft.com/d132bff1-24de-4e43-859b-2425ba7de8f0">ITfInputProcessorProfiles::AddLanguageProfile
      </a>
 

 

