---
UID: NN:wbemcli.IWbemStatusCodeText
title: IWbemStatusCodeText
author: windows-sdk-content
description: The IWbemStatusCodeText interface extracts text string descriptions of error codes or the name of the subsystem where the error occurred.
old-location: wmi\iwbemstatuscodetext.htm
tech.root: WmiSdk
ms.assetid: e196b598-6b1a-4d29-9724-2d221c4bcd16
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IWbemStatusCodeText, IWbemStatusCodeText interface [Windows Management Instrumentation], IWbemStatusCodeText interface [Windows Management Instrumentation],described, WbemStatusCodeText, _hmm_iwbemstatuscodetext, wbemcli/IWbemStatusCodeText, wmi.iwbemstatuscodetext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemStatusCodeText interface


## -description


The 
<b>IWbemStatusCodeText</b> interface extracts text string descriptions of error codes or the name of the subsystem where the error occurred.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemStatusCodeText</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemStatusCodeText</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f2adc740-f1d9-434e-a7ac-b4830350e862">GetErrorCodeText</a>
</td>
<td align="left" width="63%">
Returns the text string description associated with the error code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/831f8eb4-3dcd-42ec-aa43-309360e9a5ce">GetFacilityCodeText</a>
</td>
<td align="left" width="63%">
Returns the name of the subsystem where the error occurred.

</td>
</tr>
</table> 

