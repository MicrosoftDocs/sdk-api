---
UID: NN:wmiutils.IWbemPathKeyList
title: IWbemPathKeyList (wmiutils.h)
author: windows-sdk-content
description: Used to access the details of the path keys.
old-location: wmi\iwbempathkeylist.htm
tech.root: WmiSdk
ms.assetid: 5b188426-9d7f-4e87-9eed-ce80e5d93c30
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWbemPathKeyList, IWbemPathKeyList interface [Windows Management Instrumentation], IWbemPathKeyList interface [Windows Management Instrumentation],described, _hmm_iwbempathkeylist, wmi.iwbempathkeylist, wmiutils/IWbemPathKeyList
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemPathKeyList interface


## -description


The 
<b>IWbemPathKeyList</b> interface is used to access the details of the path keys.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemPathKeyList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemPathKeyList</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/92e78bd2-24f6-4e48-ae21-575cd1887c06">GetCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of keys in the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5df2222-988c-4f61-9b1a-9bccb647826d">GetInfo</a>
</td>
<td align="left" width="63%">
Retrieves the status bits for the key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98b3a8e6-f2cf-4a39-91f9-eb20e397e54e">GetKey</a>
</td>
<td align="left" width="63%">
Retrieves a key name or value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/009a1778-d2e3-4202-a640-60a55d5f3f8d">GetKey2</a>
</td>
<td align="left" width="63%">
Retrieves a key name or value returning the value as a VARIANT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01c69709-be6e-4a58-849d-76f9d4e3c196">GetText</a>
</td>
<td align="left" width="63%">
Retrieves the key list as text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6dd7fd31-126c-4702-8e43-3e6b08912b30">MakeSingleton</a>
</td>
<td align="left" width="63%">
Governs whether a key is singleton.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57c36ecd-7a24-4055-b373-9193fd945363">RemoveAllKeys</a>
</td>
<td align="left" width="63%">
Removes all keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07166023-2945-49d5-9d2d-8cac12053ed9">RemoveKey</a>
</td>
<td align="left" width="63%">
Removes a specified key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d655c5c7-0830-46fc-a81d-9bfa16f80d68">SetKey</a>
</td>
<td align="left" width="63%">
Sets the name or value pair for a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b282124-d544-405a-96e0-39cc504c8117">SetKey2</a>
</td>
<td align="left" width="63%">
Sets the name or value pair for a key using variants.

</td>
</tr>
</table> 

