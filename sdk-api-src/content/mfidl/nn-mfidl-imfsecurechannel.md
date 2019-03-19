---
UID: NN:mfidl.IMFSecureChannel
title: IMFSecureChannel (mfidl.h)
author: windows-sdk-content
description: Establishes a one-way secure channel between two objects.
old-location: mf\imfsecurechannel.htm
tech.root: medfound
ms.assetid: 063170b8-9483-4acd-9b42-a226e9c38f0e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 063170b8-9483-4acd-9b42-a226e9c38f0e, IMFSecureChannel, IMFSecureChannel interface [Media Foundation], IMFSecureChannel interface [Media Foundation],described, mf.imfsecurechannel, mfidl/IMFSecureChannel
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSecureChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSecureChannel interface


## -description


Establishes a one-way secure channel between two objects.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSecureChannel</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSecureChannel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSecureChannel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5465070-1706-4420-8351-fab5e8e8cd08">GetCertificate</a>
</td>
<td align="left" width="63%">
Retrieves the client's certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4d38056-ea6a-441e-8b77-39ffd316cb5a">SetupSession</a>
</td>
<td align="left" width="63%">
Passes the encrypted session key to the client.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

