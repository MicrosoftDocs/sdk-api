---
UID: NL:thrdbase.CThreadBase
title: CThreadBase (thrdbase.h)
description: The CThreadBase class is a base class that supplies the internal thread safety mechanisms for the WMI Provider Framework. This class is called internally.
helpviewer_keywords: ["??1CThreadBase@@UAE@XZ","CThreadBase","CThreadBase class [Windows Management Instrumentation]","CThreadBase class [Windows Management Instrumentation]","described","thrdbase/CThreadBase","wmi.cthreadbase"]
old-location: wmi\cthreadbase.htm
tech.root: WmiSdk
ms.assetid: 0511cd5b-f791-4821-8d75-23b0635e2266
ms.date: 12/05/2018
ms.keywords: ??1CThreadBase@@UAE@XZ, CThreadBase, CThreadBase class [Windows Management Instrumentation], CThreadBase class [Windows Management Instrumentation],described, thrdbase/CThreadBase, wmi.cthreadbase
f1_keywords:
- thrdbase/CThreadBase
dev_langs:
- c++
req.header: thrdbase.h
req.include-header: FwCommon.h
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
- DllExport
api_location:
- FrameDynOS.dll
- FrameDyn.dll
api_name:
- CThreadBase
- ??1CThreadBase@@UAE@XZ
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CThreadBase class


## -description


<p class="CCE_Message">[The <b>CThreadBase</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>CThreadBase</b> class is a base class that supplies the internal thread safety mechanisms for the WMI Provider Framework. This class is called internally.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">CThreadBase</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Enumerations</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="enums"></a>Enumerations</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">CThreadBase</b> class has these enumerations.
<table>
<tr>
<th align="left" width="37%">Enumeration</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/mt432263(v=vs.85)">FlagDefs</a>
</td>
<td align="left" width="63%">
Specifies which flags are valid for the specified type of operation. This enumeration is used by the <a href="https://docs.microsoft.com/windows/desktop/api/provider/nf-provider-provider-validateflags">Provider::ValidateFlags</a> method.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>CThreadBase</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/thrdbase/nf-thrdbase-cthreadbase-beginread">BeginRead</a>
</td>
<td align="left" width="63%">
Provides thread safety for WMI provider data access when the provider is built on the WMI Provider Framework.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/thrdbase/nf-thrdbase-cthreadbase-beginwrite">BeginWrite</a>
</td>
<td align="left" width="63%">
Provides thread safety for WMI provider operations that write data when the provider is built on the WMI Provider Framework.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/thrdbase/nf-thrdbase-cthreadbase-cthreadbase">CThreadBase</a>
</td>
<td align="left" width="63%">
Initializes a new instance of <b>CThreadBase</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/thrdbase/nf-thrdbase-cthreadbase-endread">EndRead</a>
</td>
<td align="left" width="63%">
Provides thread safety by indicating the end of a data read operation when the provider is built on the WMI Provider Framework.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/thrdbase/nf-thrdbase-cthreadbase-endwrite">EndWrite</a>
</td>
<td align="left" width="63%">
Provides thread safety by indicating the end of a data write operation when the provider is built on the WMI Provider Framework.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/thrdbase/nf-thrdbase-cthreadbase-onfinalrelease">OnFinalRelease</a>
</td>
<td align="left" width="63%">
Virtual function called by <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> when the reference count reaches zero.

</td>
</tr>
</table> 


## -remarks



The destructor for the class is <b>CWbemGlueFactory::~CWbemGlueFactory</b>.



