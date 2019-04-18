---
UID: NN:mfidl.IMFProtectedEnvironmentAccess
title: IMFProtectedEnvironmentAccess (mfidl.h)
author: windows-sdk-content
description: Provides a method that allows content protection systems to perform a handshake with the protected environment. This is needed because the CreateFile and DeviceIoControl APIs are not available to Windows Store apps.
old-location: mf\imfprotectedenvironmentaccess.htm
tech.root: medfound
ms.assetid: 2cd93bc9-4a42-4e16-80aa-4ecf5900f5e4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFProtectedEnvironmentAccess, IMFProtectedEnvironmentAccess interface [Media Foundation], IMFProtectedEnvironmentAccess interface [Media Foundation],described, mf.imfprotectedenvironmentaccess, mfidl/IMFProtectedEnvironmentAccess
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - mfidl.h
api_name:
 - IMFProtectedEnvironmentAccess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFProtectedEnvironmentAccess interface


## -description


Provides a method that allows content protection systems to perform a handshake with the protected environment. This is needed because the <b>CreateFile</b> and <b>DeviceIoControl</b> APIs are not available to Windows Store apps.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFProtectedEnvironmentAccess</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFProtectedEnvironmentAccess</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFProtectedEnvironmentAccess</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/805473c4-a2c9-483a-9a2c-29a9c63dd58c">Call</a>
</td>
<td align="left" width="63%">
Allows content protection systems to access the protected environment.

</td>
</tr>
</table> 


## -remarks



See  <a href="https://msdn.microsoft.com/B16BEFFD-26CF-4598-96A4-098C3E3AA51C">MFCreateProtectedEnvironmentAccess</a> for an example of how to create and use an <b>IMFProtectedEnvironmentAccess</b> object.




## -see-also




<a href="https://msdn.microsoft.com/B16BEFFD-26CF-4598-96A4-098C3E3AA51C">MFCreateProtectedEnvironmentAccess</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

