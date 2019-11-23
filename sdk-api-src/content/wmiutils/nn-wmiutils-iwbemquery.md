---
UID: NN:wmiutils.IWbemQuery
title: IWbemQuery (wmiutils.h)

description: Provides an entry point through which a WMI Query Language (WQL) query can be parsed.
old-location: wmi\iwbemquery.htm
tech.root: WmiSdk
ms.assetid: 4a0c0c1d-3d84-491f-8379-d164821fa71b

ms.date: 12/05/2018
ms.keywords: IWbemQuery, IWbemQuery interface [Windows Management Instrumentation], IWbemQuery interface [Windows Management Instrumentation],described, WbemQuery, _hmm_iwbemquery, wmi.iwbemquery, wmiutils/IWbemQuery
ms.topic: interface
f1_keywords: 
 - "wmiutils/IWbemQuery"
dev_langs:
 - c++
req.header: wmiutils.h
req.include-header: 
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
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiutils.dll
api_name:
 - IWbemQuery
 - IWbemQuery.GetQueryInfo
 - IWbemQuery.SetLanguageFeatures
 - IWbemQuery.TestLanguageFeatures
 - WbemQuery
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemQuery interface


## -description


The 
<b>IWbemQuery</b> interface provides an entry point through which a <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/gloss-w">WMI Query Language</a> (WQL) query can be parsed. For more information about WQL, see <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/wql-sql-for-wmi">WQL (SQL for WMI</a>).

The following table lists the methods for 
<b>IWbemQuery</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemQuery</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemQuery</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemQuery</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbemquery-empty">Empty</a>
</td>
<td align="left" width="63%">
Frees the memory that the parser is holding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbemquery-freememory">FreeMemory</a>
</td>
<td align="left" width="63%">
Frees the memory that the parser returned to the caller in the previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbemquery-getanalysis">GetAnalysis</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbemquery-getanalysis">GetAnalysis</a>
</td>
<td align="left" width="63%">
Gets the results of a successfully parsed query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>GetQueryInfo</b></td>
<td align="left" width="63%">
Not implemented. Returns <b>E_NOTIMPL</b> if called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbemquery-parse">Parse</a>
</td>
<td align="left" width="63%">
Parses a query string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>SetLanguageFeatures</b></td>
<td align="left" width="63%">
Not implemented. Returns <b>E_NOTIMPL</b> if called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>TestLanguageFeatures</b></td>
<td align="left" width="63%">
Not implemented. Returns <b>E_NOTIMPL</b> if called.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/querying-with-wql">Querying with WQL</a>
 

 

