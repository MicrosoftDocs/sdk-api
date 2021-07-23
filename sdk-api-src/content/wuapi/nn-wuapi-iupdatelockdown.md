---
UID: NN:wuapi.IUpdateLockdown
title: IUpdateLockdown (wuapi.h)
description: Restricts access to methods and properties of objects that implements the method of this interface.
helpviewer_keywords: ["IUpdateLockdown","IUpdateLockdown interface [Windows Update Agent]","IUpdateLockdown interface [Windows Update Agent]","described","wua.iupdatelockdown","wuapi/IUpdateLockdown"]
old-location: wua\iupdatelockdown.htm
tech.root: wua
ms.assetid: 918a46f5-a1da-4f47-84f1-b715fc97bb8f
ms.date: 12/05/2018
ms.keywords: IUpdateLockdown, IUpdateLockdown interface [Windows Update Agent], IUpdateLockdown interface [Windows Update Agent],described, wua.iupdatelockdown, wuapi/IUpdateLockdown
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdateLockdown
 - wuapi/IUpdateLockdown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateLockdown
---

# IUpdateLockdown interface


## -description

Restricts access to methods and properties of objects that implements the method of this interface.

## -inheritance

The <b>IUpdateLockdown</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUpdateLockdown</b> also has these types of members:

## -remarks

The <b>IUpdateLockdown</b> interface is derived from <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, not <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>. It cannot be accessed by using a script. This interface restricts access to the Windows Update  website.

The following classes implement the <b>IUpdateLockdown</b> interface:



<ul>
<li>AutomaticUpdates</li>
<li>UpdateDownloader</li>
<li>UpdateInstaller</li>
<li>UpdateServiceManager</li>
<li>WebProxy</li>
</ul>
