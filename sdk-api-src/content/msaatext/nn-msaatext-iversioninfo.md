---
UID: NN:msaatext.IVersionInfo
title: IVersionInfo (msaatext.h)
description: Exposes methods that supply version information for accessible elements.
helpviewer_keywords: ["IVersionInfo","IVersionInfo interface [Windows Accessibility]","IVersionInfo interface [Windows Accessibility]","described","msaa.iversioninfo","msaatext/IVersionInfo","winauto.iversioninfo"]
old-location: winauto\iversioninfo.htm
tech.root: WinAuto
ms.assetid: a149466a-a274-495a-a6cd-1553205abc07
ms.date: 12/05/2018
ms.keywords: IVersionInfo, IVersionInfo interface [Windows Accessibility], IVersionInfo interface [Windows Accessibility],described, msaa.iversioninfo, msaatext/IVersionInfo, winauto.iversioninfo
f1_keywords:
- msaatext/IVersionInfo
dev_langs:
- c++
req.header: msaatext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- msaatext.h
api_name:
- IVersionInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVersionInfo interface


## -description


<p class="CCE_Message">[Active Accessibility Text Services is deprecated. Please see     
<a href="https://msdn.microsoft.com/library/ms629032(VS.85).aspx">Microsoft Windows Text Services Framework</a>for more information on advanced text input and natural language technologies.
		]

Exposes methods that supply version information for accessible elements.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVersionInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVersionInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVersionInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msaatext/nf-msaatext-iversioninfo-getbuildversion">GetBuildVersion</a>
</td>
<td align="left" width="63%">
Retrieves the build version.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msaatext/nf-msaatext-iversioninfo-getcomponentdescription">GetComponentDescription</a>
</td>
<td align="left" width="63%">
Retrieves a description of the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msaatext/nf-msaatext-iversioninfo-getimplementationid">GetImplementationID</a>
</td>
<td align="left" width="63%">
Retrieves an implementation identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msaatext/nf-msaatext-iversioninfo-getinstancedescription">GetInstanceDescription</a>
</td>
<td align="left" width="63%">
Retrieves a description of the instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msaatext/nf-msaatext-iversioninfo-getsubcomponentcount">GetSubcomponentCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of subcomponents for which version information is returned.

</td>
</tr>
</table> 

