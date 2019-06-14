---
UID: NN:strmif.IAMPluginControl
title: IAMPluginControl (strmif.h)
author: windows-sdk-content
description: Controls the preferred and blocked filter lists.
old-location: dshow\iamplugincontrol.htm
tech.root: DirectShow
ms.assetid: 66720991-3a3f-4c45-a543-b8050d31fcc3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMPluginControl, IAMPluginControl interface [DirectShow], IAMPluginControl interface [DirectShow],described, dshow.iamplugincontrol, strmif/IAMPluginControl
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMPluginControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMPluginControl interface


## -description


Controls the preferred and blocked filter lists.

To get a pointer to this interface, call <b>CoCreateInstance</b>. The class identifier (CLSID) is <b>CLSID_DirectShowPluginControl</b>, which is defined in the header file uuids.h.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMPluginControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMPluginControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMPluginControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/nf-strmif-iamplugincontrol-getdisabledbyindex">IAMPluginControl::GetDisabledByIndex</a>
</td>
<td align="left" width="63%">
Gets a CLSID from the blocked list.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamplugincontrol-getpreferredclsid">IAMPluginControl::GetPreferredClsid</a>
</td>
<td align="left" width="63%">
Searches the preferred list for a CLSID that matches a specified subtype.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/nf-strmif-iamplugincontrol-getpreferredclsidbyindex">IAMPluginControl::GetPreferredClsidByIndex</a>
</td>
<td align="left" width="63%">
Gets a CLSID from the preferred list, specified by index value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamplugincontrol-isdisabled">IAMPluginControl::IsDisabled</a>
</td>
<td align="left" width="63%">
Queries whether a CLSID appears in the blocked list.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamplugincontrol-islegacydisabled">IAMPluginControl::IsLegacyDisabled</a>
</td>
<td align="left" width="63%">
Queries whether an Audio Compression Manager (ACM) or Video Compression Manager (VCM) codec appears in the blocked list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamplugincontrol-setdisabled">IAMPluginControl::SetDisabled</a>
</td>
<td align="left" width="63%">
Adds a CLSID to the blocked list, or removes a CLSID from the list.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamplugincontrol-setpreferredclsid">IAMPluginControl::SetPreferredClsid</a>
</td>
<td align="left" width="63%">
Adds a CLSID to the preferred list or removes a CLSID from the list.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/intelligent-connect">Intelligent Connect</a>
 

 

