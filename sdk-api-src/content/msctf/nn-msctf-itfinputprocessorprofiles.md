---
UID: NN:msctf.ITfInputProcessorProfiles
title: ITfInputProcessorProfiles
author: windows-sdk-content
description: The ITfInputProcessorProfiles interface is implemented by the TSF manager and used by an application or text service to manipulate the language profile of one or more text services.
old-location: tsf\itfinputprocessorprofiles.htm
old-project: TSF
ms.assetid: 9fa722a4-1e3f-4845-aea7-3b24b517f2a5
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITfInputProcessorProfiles, ITfInputProcessorProfiles interface [Text Services Framework], ITfInputProcessorProfiles interface [Text Services Framework],described, _tsf_itfinputprocessorprofiles_ref, msctf/ITfInputProcessorProfiles, tsf.itfinputprocessorprofiles
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfInputProcessorProfiles
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfInputProcessorProfiles interface


## -description


The <b>ITfInputProcessorProfiles</b> interface is implemented by the TSF manager and used by an application or text service to manipulate the language profile of one or more text services.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfInputProcessorProfiles</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfInputProcessorProfiles</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d25e5a11-8394-4fc5-b210-afa753223307">ActivateLanguageProfile</a>
</td>
<td align="left" width="63%">
Sets the active text service for a specific language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d132bff1-24de-4e43-859b-2425ba7de8f0">AddLanguageProfile</a>
</td>
<td align="left" width="63%">
Creates a language profile that consists of a specific text service and a specific language identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a0a6aa2-9015-4150-bbcf-e3f7218d53e8">ChangeCurrentLanguage</a>
</td>
<td align="left" width="63%">
Sets the currently active language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54aa6668-e577-4d75-9461-b604e1e73a78">EnableLanguageProfile</a>
</td>
<td align="left" width="63%">
Enables or disables a language profile for the current user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ab40219-278d-4721-88a1-b0bd2e3d8d2f">EnableLanguageProfileByDefault</a>
</td>
<td align="left" width="63%">
Enables or disables a language profile by default for all users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55b85ff3-35da-4126-861a-2aa4e2e8422f">EnumInputProcessorInfo</a>
</td>
<td align="left" width="63%">
Obtains an enumerator that contains the class identifiers of all registered text services.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f7c970c-3f87-4f55-b13e-12fa8b89c362">EnumLanguageProfiles</a>
</td>
<td align="left" width="63%">
Obtains an enumerator that contains all of the profiles for a specific langauage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/446bfda3-63d9-4070-b758-bdaf267c9911">GetActiveLanguageProfile</a>
</td>
<td align="left" width="63%">
Obtains the identifier of the currently active language profile for a specific text service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c770872f-752f-4c34-8d0d-cdf3d5c7d6b4">GetCurrentLanguage</a>
</td>
<td align="left" width="63%">
Obtains the identifier of the currently active language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a846505e-d6d5-4462-b420-f36fd2051d92">GetDefaultLanguageProfile</a>
</td>
<td align="left" width="63%">
Obtains the default profile for a specific language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dffca277-1c2c-4e3d-965f-42e7907ba603">GetLanguageList</a>
</td>
<td align="left" width="63%">
Obtains a list of the installed languages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5838d26-1065-498c-8361-8929c07fc725">GetLanguageProfileDescription</a>
</td>
<td align="left" width="63%">
Obtains the description string for a language profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9daaa5bf-3eb8-416f-b7f5-9b10c04bceb0">IsEnabledLanguageProfile</a>
</td>
<td align="left" width="63%">
Determines if a specific language profile is enabled or disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/264bc32e-60a2-4dff-a212-5682d30a769e">Register</a>
</td>
<td align="left" width="63%">
Adds a text service to TSF.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16eff9bc-1789-4bf6-b1ba-b7e8414ce080">RemoveLanguageProfile</a>
</td>
<td align="left" width="63%">
Removes a language profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/385bf5d6-6541-483d-8286-1ba759616fc6">SetDefaultLanguageProfile</a>
</td>
<td align="left" width="63%">
Sets the default profile for a specific language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e069f515-d5f6-4acd-a3ff-0c3c60c785ac">SubstituteKeyboardLayout</a>
</td>
<td align="left" width="63%">
Sets a substitute keyboard layout for the specified language profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53de09dd-3d99-4968-8861-397b67daf8c5">Unregister</a>
</td>
<td align="left" width="63%">
Removes a text service from TSF.

</td>
</tr>
</table> 


## -remarks



To obtain a pointer to this interface, call <a href="_com_cocreateinstance">CoCreateInstance</a> with CLSID_TF_InputProcessorProfiles.


#### Examples

<b>ITfInputProcessorProfiles</b>

<div class="code"></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT hr;
ITfInputProcessorProfiles *pProfiles;

//Create the object. 
hr = CoCreateInstance(  CLSID_TF_InputProcessorProfiles, 
                        NULL, 
                        CLSCTX_INPROC_SERVER, 
                        IID_ITfInputProcessorProfiles, 
                        (LPVOID*)&amp;pProfiles);

if(SUCCEEDED(hr))
{
    //Use the interface. 

    //Release the interface. 
    pProfiles-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>


