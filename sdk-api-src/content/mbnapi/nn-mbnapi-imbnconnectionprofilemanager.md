---
UID: NN:mbnapi.IMbnConnectionProfileManager
title: IMbnConnectionProfileManager (mbnapi.h)
author: windows-sdk-content
description: Provides access to connection profiles and connection notifications.
old-location: mbn\imbnconnectionprofilemanager.htm
tech.root: mbn
ms.assetid: a55e4183-f914-4064-a391-3bd31ca59160
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnConnectionProfileManager, IMbnConnectionProfileManager interface [Microsoft Broadband Networks], IMbnConnectionProfileManager interface [Microsoft Broadband Networks],described, mbn.imbnconnectionprofilemanager, mbnapi/IMbnConnectionProfileManager
ms.topic: interface
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
 - IMbnConnectionProfileManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnConnectionProfileManager interface


## -description


Provides access to connection profiles and connection notifications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnConnectionProfileManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnConnectionProfileManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnConnectionProfileManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile">CreateConnectionProfile</a>
</td>
<td align="left" width="63%">
Creates a new connection profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-getconnectionprofile">GetConnectionProfile</a>
</td>
<td align="left" width="63%">
Gets a specific connection profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-getconnectionprofiles">GetConnectionProfiles</a>
</td>
<td align="left" width="63%">
Gets a list of connection profiles.

</td>
</tr>
</table> 


## -remarks



This interface can be used to access the following notification interfaces.<table>
<tr>
<th>Notification Sink to Register   </th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanagerevents">IMbnConnectionProfileManagerEvents</a>
</td>
<td><b>IID_IMbnConnectionProfileManagerEvents</b></td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofileevents">MbnConnectionProfileEvents</a>
</td>
<td><b>IID_IMbnConnectionProfileEvents</b></td>
</tr>
</table>
 



An application can obtain this interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with a class id of <b>CLSID_IMbnConnectionProfileManager</b>.

The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <b>IMbnConnectionProfileManager</b> object.</li>
<li>
For each notification sink to register, call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass IID corresponding to the notification sink to <i>riid</i>.

</li>
<li>For each connection point returned by step 2, call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements the matching notification interface to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



