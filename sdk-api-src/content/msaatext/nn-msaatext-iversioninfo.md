---
UID: NN:msaatext.IVersionInfo
title: IVersionInfo
author: windows-sdk-content
description: Exposes methods that supply version information for accessible elements.
old-location: winauto\iversioninfo.htm
tech.root: WinAuto
ms.assetid: a149466a-a274-495a-a6cd-1553205abc07
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IVersionInfo, IVersionInfo interface [Windows Accessibility], IVersionInfo interface [Windows Accessibility],described, msaa.iversioninfo, msaatext/IVersionInfo, winauto.iversioninfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVersionInfo interface


## -description


<p class="CCE_Message">[Active Accessibility Text Services is deprecated. Please see     
<a href="https://go.microsoft.com/fwlink/p/?linkid=131573">Microsoft Windows Text Services Framework</a>for more information on advanced text input and natural language technologies.
		]

Exposes methods that supply version information for accessible elements.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVersionInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVersionInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ae54ad59-665c-494c-8054-3f19aec9968f">GetBuildVersion</a>
</td>
<td align="left" width="63%">
Retrieves the build version.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb689adb-bd94-4c62-b408-33e1aa694c89">GetComponentDescription</a>
</td>
<td align="left" width="63%">
Retrieves a description of the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/018834df-bd03-4bf5-8af2-b325f7a6a586">GetImplementationID</a>
</td>
<td align="left" width="63%">
Retrieves an implementation identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8aa3fd3-9869-4c24-8c9a-752947d21002">GetInstanceDescription</a>
</td>
<td align="left" width="63%">
Retrieves a description of the instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1a169f1-db47-4c5b-9515-1f2660cfae17">GetSubcomponentCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of subcomponents for which version information is returned.

</td>
</tr>
</table> 

