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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFProtectedEnvironmentAccess</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFProtectedEnvironmentAccess</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfprotectedenvironmentaccess-call">Call</a>
</td>
<td align="left" width="63%">
Allows content protection systems to access the protected environment.

</td>
</tr>
</table> 


## -remarks



See  <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreateprotectedenvironmentaccess">MFCreateProtectedEnvironmentAccess</a> for an example of how to create and use an <b>IMFProtectedEnvironmentAccess</b> object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreateprotectedenvironmentaccess">MFCreateProtectedEnvironmentAccess</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

