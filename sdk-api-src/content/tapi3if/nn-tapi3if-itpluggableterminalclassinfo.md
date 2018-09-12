---
UID: NN:tapi3if.ITPluggableTerminalClassInfo
title: ITPluggableTerminalClassInfo
author: windows-sdk-content
description: The ITPluggableTerminalClassInfo interface exposes methods that allow the application to retrieve information concerning a pluggable terminal.
old-location: tapi3\itpluggableterminalclassinfo.htm
tech.root: tapi
ms.assetid: 0f7190c4-c696-4749-82f2-20fdbc8651f4
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITPluggableTerminalClassInfo, ITPluggableTerminalClassInfo interface [TAPI 2.2], ITPluggableTerminalClassInfo interface [TAPI 2.2],described, _tapi3_itpluggableterminalclassinfo, tapi3.itpluggableterminalclassinfo, tapi3if/ITPluggableTerminalClassInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPluggableTerminalClassInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPluggableTerminalClassInfo interface


## -description


The 
<b>ITPluggableTerminalClassInfo</b> interface exposes methods that allow the application to retrieve information concerning a pluggable terminal.

The 
<a href="https://msdn.microsoft.com/6a661738-06e9-49b8-948a-02c61c621fdd">IEnumPluggableTerminalClassInfo::Next</a> and 
<a href="https://msdn.microsoft.com/4bbb7f77-fc67-4b6b-88fa-2dc5bcfb6c48">ITTerminalSupport2::get_PluggableTerminalClasses</a> methods create the 
<b>ITPluggableTerminalClassInfo</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPluggableTerminalClassInfo</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITPluggableTerminalClassInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITPluggableTerminalClassInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17513c0f-bc3a-474b-a9e0-ea91e2ae7fbf">get_CLSID</a>
</td>
<td align="left" width="63%">
Gets the CLSID used to CoCreateInstance the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5595b18-264f-437f-8533-b7c87e6e7d00">get_Company</a>
</td>
<td align="left" width="63%">
Gets the name of the company that issued this pluggable terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/843aeedc-08ca-436b-9d43-1e7b9aa1ac8e">get_Direction</a>
</td>
<td align="left" width="63%">
Gets the direction supported by the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c17540f-b899-4768-b0a2-2ab11f34636c">get_MediaTypes</a>
</td>
<td align="left" width="63%">
Gets the media types supported by the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97bd38f3-27d8-4618-9138-bd972db9abb9">get_Name</a>
</td>
<td align="left" width="63%">
Gets the terminal's friendly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7dfa6cf8-23b8-4959-ba39-6efda1d71562">get_TerminalClass</a>
</td>
<td align="left" width="63%">
Gets the terminal's terminal class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e87ebf36-dace-4318-8d45-87f7a451284e">get_Version</a>
</td>
<td align="left" width="63%">
Gets the terminal version.

</td>
</tr>
</table> 

