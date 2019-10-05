---
UID: NN:wmiutils.IWbemPathKeyList
title: IWbemPathKeyList (wmiutils.h)
author: windows-sdk-content
description: Used to access the details of the path keys.
old-location: wmi\iwbempathkeylist.htm
tech.root: WmiSdk
ms.assetid: 5b188426-9d7f-4e87-9eed-ce80e5d93c30
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWbemPathKeyList, IWbemPathKeyList interface [Windows Management Instrumentation], IWbemPathKeyList interface [Windows Management Instrumentation],described, _hmm_iwbempathkeylist, wmi.iwbempathkeylist, wmiutils/IWbemPathKeyList
ms.topic: interface
f1_keywords: 
 - "wmiutils/IWbemPathKeyList"
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
 - IWbemPathKeyList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemPathKeyList interface


## -description


The 
<b>IWbemPathKeyList</b> interface is used to access the details of the path keys.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemPathKeyList</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemPathKeyList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemPathKeyList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempathkeylist-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of keys in the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempathkeylist-getinfo">GetInfo</a>
</td>
<td align="left" width="63%">
Retrieves the status bits for the key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempathkeylist-getkey">GetKey</a>
</td>
<td align="left" width="63%">
Retrieves a key name or value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempathkeylist-getkey2">GetKey2</a>
</td>
<td align="left" width="63%">
Retrieves a key name or value returning the value as a VARIANT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempathkeylist-gettext">GetText</a>
</td>
<td align="left" width="63%">
Retrieves the key list as text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempathkeylist-makesingleton">MakeSingleton</a>
</td>
<td align="left" width="63%">
Governs whether a key is singleton.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempathkeylist-removeallkeys">RemoveAllKeys</a>
</td>
<td align="left" width="63%">
Removes all keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempathkeylist-removekey">RemoveKey</a>
</td>
<td align="left" width="63%">
Removes a specified key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempathkeylist-setkey">SetKey</a>
</td>
<td align="left" width="63%">
Sets the name or value pair for a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempathkeylist-setkey2">SetKey2</a>
</td>
<td align="left" width="63%">
Sets the name or value pair for a key using variants.

</td>
</tr>
</table> 

