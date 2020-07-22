---
UID: NL:objpath.CObjectPathParser
title: CObjectPathParser (objpath.h)
description: Parses a WMI path which can include a remote computer name, namespaces, and classes. Use of this object is not recommended. Instead, use the IWbemPath COM interface.
helpviewer_keywords: ["??1CObjectPathParser@@QAE@XZ","??1CObjectPathParser@@QEAA@XZ","CObjectPathParser","CObjectPathParser class [Windows Management Instrumentation]","CObjectPathParser class [Windows Management Instrumentation]","described","objpath/CObjectPathParser","wmi.cobjectpathparser"]
old-location: wmi\cobjectpathparser.htm
tech.root: wmi
ms.assetid: 0138c48f-f61b-4127-adc2-bdf4da06f938
ms.date: 12/05/2018
ms.keywords: ??1CObjectPathParser@@QAE@XZ, ??1CObjectPathParser@@QEAA@XZ, CObjectPathParser, CObjectPathParser class [Windows Management Instrumentation], CObjectPathParser class [Windows Management Instrumentation],described, objpath/CObjectPathParser, wmi.cobjectpathparser
f1_keywords:
- objpath/CObjectPathParser
dev_langs:
- c++
req.header: objpath.h
req.include-header: ObjPath.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
api_name:
- CObjectPathParser
- ??1CObjectPathParser@@QAE@XZ
- ??1CObjectPathParser@@QEAA@XZ
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CObjectPathParser class


## -description


<p class="CCE_Message">[The <b>CObjectPathParser</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

Parses a WMI path which can include a remote computer name, namespaces, and classes. Use of this object is not recommended. Instead, use the <a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a> COM interface.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">CObjectPathParser</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">CObjectPathParser</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objpath/nf-objpath-cobjectpathparser-cobjectpathparser">CObjectPathParser</a>
</td>
<td align="left" width="63%">
Constructs and initializes an instance of a <b>CObjectPathParser</b> object.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>CObjectPathParser</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb204795(v=vs.85)">Free</a>
</td>
<td align="left" width="63%">Overloaded. Releases the memory that contains the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objpath/nf-objpath-cobjectpathparser-parse">Parse</a>
</td>
<td align="left" width="63%">
Parses a string that contains a WMI path into a structure the contains the path parts, such as the server, namespace, class, key that identifies an instance, and others.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objpath/nf-objpath-cobjectpathparser-unparse">UnParse</a>
</td>
<td align="left" width="63%">
Converts a structure that contains the parsed path to a string.

</td>
</tr>
</table> 

