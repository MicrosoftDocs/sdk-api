---
UID: NN:msctf.ITfInputProcessorProfiles
title: ITfInputProcessorProfiles (msctf.h)
author: windows-sdk-content
description: The ITfInputProcessorProfiles interface is implemented by the TSF manager and used by an application or text service to manipulate the language profile of one or more text services.
old-location: tsf\itfinputprocessorprofiles.htm
tech.root: TSF
ms.assetid: 9fa722a4-1e3f-4845-aea7-3b24b517f2a5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfiles, ITfInputProcessorProfiles interface [Text Services Framework], ITfInputProcessorProfiles interface [Text Services Framework],described, _tsf_itfinputprocessorprofiles_ref, msctf/ITfInputProcessorProfiles, tsf.itfinputprocessorprofiles
ms.topic: interface
f1_keywords: 
 - "msctf/ITfInputProcessorProfiles"
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfInputProcessorProfiles
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfInputProcessorProfiles interface


## -description


The <b>ITfInputProcessorProfiles</b> interface is implemented by the TSF manager and used by an application or text service to manipulate the language profile of one or more text services.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfInputProcessorProfiles</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfInputProcessorProfiles</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfInputProcessorProfiles</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-activatelanguageprofile">ActivateLanguageProfile</a>
</td>
<td align="left" width="63%">
Sets the active text service for a specific language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile">AddLanguageProfile</a>
</td>
<td align="left" width="63%">
Creates a language profile that consists of a specific text service and a specific language identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-changecurrentlanguage">ChangeCurrentLanguage</a>
</td>
<td align="left" width="63%">
Sets the currently active language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-enablelanguageprofile">EnableLanguageProfile</a>
</td>
<td align="left" width="63%">
Enables or disables a language profile for the current user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-enablelanguageprofilebydefault">EnableLanguageProfileByDefault</a>
</td>
<td align="left" width="63%">
Enables or disables a language profile by default for all users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-enuminputprocessorinfo">EnumInputProcessorInfo</a>
</td>
<td align="left" width="63%">
Obtains an enumerator that contains the class identifiers of all registered text services.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-enumlanguageprofiles">EnumLanguageProfiles</a>
</td>
<td align="left" width="63%">
Obtains an enumerator that contains all of the profiles for a specific langauage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-getactivelanguageprofile">GetActiveLanguageProfile</a>
</td>
<td align="left" width="63%">
Obtains the identifier of the currently active language profile for a specific text service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-getcurrentlanguage">GetCurrentLanguage</a>
</td>
<td align="left" width="63%">
Obtains the identifier of the currently active language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-getdefaultlanguageprofile">GetDefaultLanguageProfile</a>
</td>
<td align="left" width="63%">
Obtains the default profile for a specific language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-getlanguagelist">GetLanguageList</a>
</td>
<td align="left" width="63%">
Obtains a list of the installed languages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-getlanguageprofiledescription">GetLanguageProfileDescription</a>
</td>
<td align="left" width="63%">
Obtains the description string for a language profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-isenabledlanguageprofile">IsEnabledLanguageProfile</a>
</td>
<td align="left" width="63%">
Determines if a specific language profile is enabled or disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register">Register</a>
</td>
<td align="left" width="63%">
Adds a text service to TSF.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile">RemoveLanguageProfile</a>
</td>
<td align="left" width="63%">
Removes a language profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-setdefaultlanguageprofile">SetDefaultLanguageProfile</a>
</td>
<td align="left" width="63%">
Sets the default profile for a specific language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-substitutekeyboardlayout">SubstituteKeyboardLayout</a>
</td>
<td align="left" width="63%">
Sets a substitute keyboard layout for the specified language profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-unregister">Unregister</a>
</td>
<td align="left" width="63%">
Removes a text service from TSF.

</td>
</tr>
</table> 


## -remarks



To obtain a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with CLSID_TF_InputProcessorProfiles.


#### Examples

<b>ITfInputProcessorProfiles</b>

<div class="code"></div>

```cpp

HRESULT hr;
ITfInputProcessorProfiles *pProfiles;

//Create the object. 
hr = CoCreateInstance(  CLSID_TF_InputProcessorProfiles, 
                        NULL, 
                        CLSCTX_INPROC_SERVER, 
                        IID_ITfInputProcessorProfiles, 
                        (LPVOID*)&pProfiles);

if(SUCCEEDED(hr))
{
    //Use the interface. 

    //Release the interface. 
    pProfiles->Release();
}

```




