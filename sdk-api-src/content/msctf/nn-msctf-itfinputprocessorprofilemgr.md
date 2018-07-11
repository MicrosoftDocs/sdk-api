---
UID: NN:msctf.ITfInputProcessorProfileMgr
title: ITfInputProcessorProfileMgr
author: windows-sdk-content
description: The ITfInputProcessorProfileMgr interface is implemented by the TSF manager and used by an application or text service to manipulate the language profile of one or more text services.
old-location: tsf\itfinputprocessorprofilemgr.htm
old-project: TSF
ms.assetid: d60bb748-3c61-466d-9c17-df7bc4904994
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfInputProcessorProfileMgr, ITfInputProcessorProfileMgr interface [Text Services Framework], ITfInputProcessorProfileMgr interface [Text Services Framework],described, _tsf_itfinputprocessorprofilemgr_ref, msctf/ITfInputProcessorProfileMgr, tsf.itfinputprocessorprofilemgr
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.h
api_name:
 - ITfInputProcessorProfileMgr
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfInputProcessorProfileMgr interface


## -description


The <b>ITfInputProcessorProfileMgr</b> interface is implemented by the TSF manager and used by an application or text service to manipulate the language profile of one or more text services.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfInputProcessorProfileMgr</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfInputProcessorProfileMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfInputProcessorProfileMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e5b3f26-332a-456e-875f-12e440ae67ba">ActivateProfile</a>
</td>
<td align="left" width="63%">
Activates the specified text service or keyboard layout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d2bd329-1b17-4b03-8c75-74d99ccc0f08">DeactivateProfile</a>
</td>
<td align="left" width="63%">
Deactivates the specified text service or keyboard layout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4728d12-9073-41b8-94bc-eaf7c1df19b6">EnumProfiles</a>
</td>
<td align="left" width="63%">
Enumerates input processor profiles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4fd03327-c0c4-4dd6-b68a-8faae48c9a3d">GetActiveProfile</a>
</td>
<td align="left" width="63%">
Retrieves the current active profile for the category.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/581bddf5-3def-48c6-a092-4f751142cc1b">GetProfile</a>
</td>
<td align="left" width="63%">
Get the profile information of the text service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b497409d-96b8-41d1-9512-5d79494c6287">RegisterProfile</a>
</td>
<td align="left" width="63%">
Registers the text service and adds the profiles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7bcc50a-9f94-4a55-aca2-db9a40be2157">ReleaseInputProcessor</a>
</td>
<td align="left" width="63%">
Releases the input processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b05beea-991a-406f-a08d-28cdd87c9d7d">UnregisterProfile</a>
</td>
<td align="left" width="63%">
Unregisters the text service and associated profiles.

</td>
</tr>
</table> 


## -remarks



Unlike <a href="https://msdn.microsoft.com/9fa722a4-1e3f-4845-aea7-3b24b517f2a5">ITfInputProcessorProfiles</a>, ITfInputProcessorProfileMgr
 can manage both keyboard layout and text services seamlessly. In Windows Vista, it is recommended to use this interface instead of using the following methods:

<ul>
<li>ITfInputProcessorProfiles::Register</li>
<li>ITfInputProcessorProfiles::Unregister</li>
<li>ITfInputProcessorProfiles::AddLanguageProfile</li>
<li>ITfInputProcessorProfiles::RemoveLanguageProfile</li>
<li>ITfInputProcessorProfiles::EnumInputProcessorInfo</li>
<li>ITfInputProcessorProfiles::ActivateLanguageProfile</li>
<li>ITfInputProcessorProfiles::GetActiveLanguageProfile</li>
<li>ITfInputProcessorProfiles::EnumLanguageProfiles</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/9fa722a4-1e3f-4845-aea7-3b24b517f2a5">ITfInputProcessorProfiles</a>
 

 

