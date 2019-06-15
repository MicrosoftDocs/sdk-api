---
UID: NN:mbnapi.IMbnConnectionProfileEvents
title: IMbnConnectionProfileEvents (mbnapi.h)
author: windows-sdk-content
description: This notification interface signals an application when IMbnConnectionProfile methods change the Mobile Broadband profile state.
old-location: mbn\imbnconnectionprofileevents.htm
tech.root: mbn
ms.assetid: 235fa0ef-4fc2-4a36-8ad7-2dceb597498f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnConnectionProfileEvents, IMbnConnectionProfileEvents interface [Microsoft Broadband Networks], IMbnConnectionProfileEvents interface [Microsoft Broadband Networks],described, mbn.imbnconnectionprofileevents, mbnapi/IMbnConnectionProfileEvents
ms.topic: interface
f1_keywords: ["mbnapi/IMbnConnectionProfileEvents"]
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnectionProfileEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnConnectionProfileEvents interface


## -description


This notification interface signals an application when <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile">IMbnConnectionProfile</a> methods change the Mobile Broadband profile state.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnConnectionProfileEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnConnectionProfileEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnConnectionProfileEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofileevents-onprofileupdate">OnProfileUpdate</a>
</td>
<td align="left" width="63%">
A profile update operation has completed.

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager">IMbnConnectionProfileManager</a> object.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnConnectionProfileEvents</b> to <i>riid</i>.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnConnectionProfileEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



