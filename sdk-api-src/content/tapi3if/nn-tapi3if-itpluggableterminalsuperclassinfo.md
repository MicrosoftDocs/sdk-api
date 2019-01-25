---
UID: NN:tapi3if.ITPluggableTerminalSuperclassInfo
title: ITPluggableTerminalSuperclassInfo
author: windows-sdk-content
description: The ITPluggableTerminalSuperclassInfo interface exposes methods that get the name and CLSID of a pluggable terminal class.
old-location: tapi3\itpluggableterminalsuperclassinfo.htm
tech.root: Tapi
ms.assetid: f9226af1-90e7-4317-af73-e1563883e2b6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITPluggableTerminalSuperclassInfo, ITPluggableTerminalSuperclassInfo interface [TAPI 2.2], ITPluggableTerminalSuperclassInfo interface [TAPI 2.2],described, _tapi3_itpluggableterminalsuperclassinfo, tapi3.itpluggableterminalsuperclassinfo, tapi3if/ITPluggableTerminalSuperclassInfo
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
 - ITPluggableTerminalSuperclassInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPluggableTerminalSuperclassInfo interface


## -description


The 
<b>ITPluggableTerminalSuperclassInfo</b> interface exposes methods that get the name and CLSID of a pluggable terminal class. The 
<a href="https://msdn.microsoft.com/820cf2cd-1354-473d-974d-267b888f07a9">IEnumPluggableSuperclassInfo::Next</a> and 
<a href="https://msdn.microsoft.com/6d66aeca-5ac2-4019-b326-71c3bfb6d28e">ITTerminalSupport2::get_PluggableSuperclasses</a> methods create the 
<b>ITPluggableTerminalSuperclassInfo</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPluggableTerminalSuperclassInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITPluggableTerminalSuperclassInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITPluggableTerminalSuperclassInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96f2fc11-43b0-4082-ab3d-d5813cd55ee2">get_CLSID</a>
</td>
<td align="left" width="63%">
Gets the CLSID used to <b>CoCreateInstance</b> the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36f1f8a9-5bde-43ea-a68a-15ea7d9415aa">get_Name</a>
</td>
<td align="left" width="63%">
Gets the terminal's friendly name.

</td>
</tr>
</table> 

