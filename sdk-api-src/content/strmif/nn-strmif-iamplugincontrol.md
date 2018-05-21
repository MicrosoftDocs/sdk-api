---
UID: NN:strmif.IAMPluginControl
title: IAMPluginControl
author: windows-driver-content
description: Controls the preferred and blocked filter lists.
old-location: dshow\iamplugincontrol.htm
old-project: DirectShow
ms.assetid: 66720991-3a3f-4c45-a543-b8050d31fcc3
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IAMPluginControl, IAMPluginControl interface [DirectShow], IAMPluginControl interface [DirectShow],described, dshow.iamplugincontrol, strmif/IAMPluginControl
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmif.h
api_name:
-	IAMPluginControl
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMPluginControl interface


## -description


Controls the preferred and blocked filter lists.

To get a pointer to this interface, call <b>CoCreateInstance</b>. The class identifier (CLSID) is <b>CLSID_DirectShowPluginControl</b>, which is defined in the header file uuids.h.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMPluginControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMPluginControl</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7c55e37b-46f1-4283-bea4-3884ae730906">IAMPluginControl::GetDisabledByIndex</a>
</td>
<td align="left" width="63%">
Gets a CLSID from the blocked list.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69f55810-9a3a-48cd-8fd2-d091a906d229">IAMPluginControl::GetPreferredClsid</a>
</td>
<td align="left" width="63%">
Searches the preferred list for a CLSID that matches a specified subtype.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50da3961-3913-4e7d-bbbc-b89450f99931">IAMPluginControl::GetPreferredClsidByIndex</a>
</td>
<td align="left" width="63%">
Gets a CLSID from the preferred list, specified by index value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d6bae28-7c26-47c4-8633-9ecc60293dc6">IAMPluginControl::IsDisabled</a>
</td>
<td align="left" width="63%">
Queries whether a CLSID appears in the blocked list.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f67c7a78-1e4f-469a-9cbb-80c37bba80b7">IAMPluginControl::IsLegacyDisabled</a>
</td>
<td align="left" width="63%">
Queries whether an Audio Compression Manager (ACM) or Video Compression Manager (VCM) codec appears in the blocked list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ac4b3b5-0882-4e30-b3fa-1dcee33a74d3">IAMPluginControl::SetDisabled</a>
</td>
<td align="left" width="63%">
Adds a CLSID to the blocked list, or removes a CLSID from the list.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45702714-6b35-4863-885e-55049258a4ae">IAMPluginControl::SetPreferredClsid</a>
</td>
<td align="left" width="63%">
Adds a CLSID to the preferred list or removes a CLSID from the list.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/938ba1b0-822e-4871-8786-b7eeee243867">Intelligent Connect</a>
 

 

