---
UID: NN:wuapi.IUpdateLockdown
title: IUpdateLockdown (wuapi.h)
author: windows-sdk-content
description: Restricts access to methods and properties of objects that implements the method of this interface.
old-location: wua\iupdatelockdown.htm
tech.root: Wua_Sdk
ms.assetid: 918a46f5-a1da-4f47-84f1-b715fc97bb8f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUpdateLockdown, IUpdateLockdown interface [Windows Update Agent], IUpdateLockdown interface [Windows Update Agent],described, wua.iupdatelockdown, wuapi/IUpdateLockdown
ms.topic: interface
f1_keywords: 
 - "wuapi/IUpdateLockdown"
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateLockdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUpdateLockdown interface


## -description


Restricts access to methods and properties of objects that implements the method of this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateLockdown</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUpdateLockdown</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUpdateLockdown</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatelockdown-lockdown">Lockdown</a>
</td>
<td align="left" width="63%">
Restricts access to the methods and properties of the object that implements this method.

</td>
</tr>
</table> 


## -remarks



The <b>IUpdateLockdown</b> interface is derived from <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, not <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>. It cannot be accessed by using a script. This interface restricts access to the Windows Update  website.

The following classes implement the <b>IUpdateLockdown</b> interface:



<ul>
<li>AutomaticUpdates</li>
<li>UpdateDownloader</li>
<li>UpdateInstaller</li>
<li>UpdateServiceManager</li>
<li>WebProxy</li>
</ul>


