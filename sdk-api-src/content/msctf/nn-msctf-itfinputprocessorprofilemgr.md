---
UID: NN:msctf.ITfInputProcessorProfileMgr
title: ITfInputProcessorProfileMgr (msctf.h)
description: The ITfInputProcessorProfileMgr interface is implemented by the TSF manager and used by an application or text service to manipulate the language profile of one or more text services.
helpviewer_keywords: ["ITfInputProcessorProfileMgr","ITfInputProcessorProfileMgr interface [Text Services Framework]","ITfInputProcessorProfileMgr interface [Text Services Framework]","described","_tsf_itfinputprocessorprofilemgr_ref","msctf/ITfInputProcessorProfileMgr","tsf.itfinputprocessorprofilemgr"]
old-location: tsf\itfinputprocessorprofilemgr.htm
tech.root: TSF
ms.assetid: d60bb748-3c61-466d-9c17-df7bc4904994
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfileMgr, ITfInputProcessorProfileMgr interface [Text Services Framework], ITfInputProcessorProfileMgr interface [Text Services Framework],described, _tsf_itfinputprocessorprofilemgr_ref, msctf/ITfInputProcessorProfileMgr, tsf.itfinputprocessorprofilemgr
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfInputProcessorProfileMgr
 - msctf/ITfInputProcessorProfileMgr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.h
api_name:
 - ITfInputProcessorProfileMgr
---

# ITfInputProcessorProfileMgr interface


## -description

The <b>ITfInputProcessorProfileMgr</b> interface is implemented by the TSF manager and used by an application or text service to manipulate the language profile of one or more text services.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfInputProcessorProfileMgr</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfInputProcessorProfileMgr</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofilemgr-activateprofile">ActivateProfile</a>
</td>
<td align="left" width="63%">
Activates the specified text service or keyboard layout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofilemgr-deactivateprofile">DeactivateProfile</a>
</td>
<td align="left" width="63%">
Deactivates the specified text service or keyboard layout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofilemgr-enumprofiles">EnumProfiles</a>
</td>
<td align="left" width="63%">
Enumerates input processor profiles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofilemgr-getactiveprofile">GetActiveProfile</a>
</td>
<td align="left" width="63%">
Retrieves the current active profile for the category.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofilemgr-getprofile">GetProfile</a>
</td>
<td align="left" width="63%">
Get the profile information of the text service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofilemgr-registerprofile">RegisterProfile</a>
</td>
<td align="left" width="63%">
Registers the text service and adds the profiles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofilemgr-releaseinputprocessor">ReleaseInputProcessor</a>
</td>
<td align="left" width="63%">
Releases the input processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofilemgr-unregisterprofile">UnregisterProfile</a>
</td>
<td align="left" width="63%">
Unregisters the text service and associated profiles.

</td>
</tr>
</table>

## -remarks

Unlike <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a>, ITfInputProcessorProfileMgr
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

<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a>

