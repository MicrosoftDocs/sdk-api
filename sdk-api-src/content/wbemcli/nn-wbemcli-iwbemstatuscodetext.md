---
UID: NN:wbemcli.IWbemStatusCodeText
title: IWbemStatusCodeText (wbemcli.h)
description: The IWbemStatusCodeText interface extracts text string descriptions of error codes or the name of the subsystem where the error occurred.helpviewer_keywords: ["IWbemStatusCodeText","IWbemStatusCodeText interface [Windows Management Instrumentation]","IWbemStatusCodeText interface [Windows Management Instrumentation]","described","WbemStatusCodeText","_hmm_iwbemstatuscodetext","wbemcli/IWbemStatusCodeText","wmi.iwbemstatuscodetext"]
old-location: wmi\iwbemstatuscodetext.htm
tech.root: WmiSdk
ms.assetid: e196b598-6b1a-4d29-9724-2d221c4bcd16
ms.date: 12/05/2018
ms.keywords: IWbemStatusCodeText, IWbemStatusCodeText interface [Windows Management Instrumentation], IWbemStatusCodeText interface [Windows Management Instrumentation],described, WbemStatusCodeText, _hmm_iwbemstatuscodetext, wbemcli/IWbemStatusCodeText, wmi.iwbemstatuscodetext
f1_keywords:
- wbemcli/IWbemStatusCodeText
dev_langs:
- c++
req.header: wbemcli.h
req.include-header: Wbemidl.h
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
- IWbemStatusCodeText
- WbemStatusCodeText
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemStatusCodeText interface


## -description


The 
<b>IWbemStatusCodeText</b> interface extracts text string descriptions of error codes or the name of the subsystem where the error occurred.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemStatusCodeText</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemStatusCodeText</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemStatusCodeText</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemstatuscodetext-geterrorcodetext">GetErrorCodeText</a>
</td>
<td align="left" width="63%">
Returns the text string description associated with the error code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemstatuscodetext-getfacilitycodetext">GetFacilityCodeText</a>
</td>
<td align="left" width="63%">
Returns the name of the subsystem where the error occurred.

</td>
</tr>
</table> 

