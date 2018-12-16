---
UID: NN:rend.ITDirectoryObjectUser
title: ITDirectoryObjectUser
author: windows-sdk-content
description: The ITDirectoryObjectUser interface is the common interface supported by the User object. This interface is created by calling QueryInterface on ITDirectoryObject.
old-location: tapi3\itdirectoryobjectuser.htm
tech.root: tapi
ms.assetid: 65356507-51d1-479d-8e93-7e18ec041ce3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITDirectoryObjectUser, ITDirectoryObjectUser interface [TAPI 2.2], ITDirectoryObjectUser interface [TAPI 2.2],described, _tapi3_itdirectoryobjectuser, rend/ITDirectoryObjectUser, tapi3.itdirectoryobjectuser
ms.topic: interface
req.header: rend.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rend.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Rend.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - ITDirectoryObjectUser
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDirectoryObjectUser interface


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>ITDirectoryObjectUser</b> interface is the common interface supported by the User object. This interface is created by calling <b>QueryInterface</b> on 
<a href="https://msdn.microsoft.com/a48644a4-43e2-4c52-84be-0cb5c49e6436">ITDirectoryObject</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITDirectoryObjectUser</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITDirectoryObjectUser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITDirectoryObjectUser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43bb9ce5-28ff-4a6f-a55c-a84633e22dfe">get_IPPhonePrimary</a>
</td>
<td align="left" width="63%">
Gets user's primary IP phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba53ea12-7f05-4f68-8a59-915a5906b7be">put_IPPhonePrimary</a>
</td>
<td align="left" width="63%">
Sets user's primary IP phone.

</td>
</tr>
</table> 

