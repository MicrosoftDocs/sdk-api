---
UID: NN:mfidl.IMFFieldOfUseMFTUnlock
title: IMFFieldOfUseMFTUnlock
author: windows-sdk-content
description: Enables an application to use a Media Foundation transform (MFT) that has restrictions on its use.
old-location: mf\imffieldofusemftunlock.htm
tech.root: medfound
ms.assetid: b144589b-d559-4686-b617-0e3c393380e9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMFFieldOfUseMFTUnlock, IMFFieldOfUseMFTUnlock interface [Media Foundation], IMFFieldOfUseMFTUnlock interface [Media Foundation],described, mf.imffieldofusemftunlock, mfidl/IMFFieldOfUseMFTUnlock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IMFFieldOfUseMFTUnlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFFieldOfUseMFTUnlock interface


## -description


Enables an application to use a Media Foundation transform (MFT) that has restrictions on its use.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFFieldOfUseMFTUnlock</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFFieldOfUseMFTUnlock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFFieldOfUseMFTUnlock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54b15e72-6551-4162-90ca-a9bed68ca62f">Unlock</a>
</td>
<td align="left" width="63%">
Unlocks an MFT so that the application can use it.

</td>
</tr>
</table> 


## -remarks



If you register an MFT that requires unlocking, include the <b>MFT_ENUM_FLAG_FIELDOFUSE</b> flag when you call the <a href="https://msdn.microsoft.com/fb3a2b67-d3e4-4d5f-960a-3979f4780904">MFTRegister</a> function.




## -see-also




<a href="https://msdn.microsoft.com/36f28e4c-2baf-4618-9935-5d4615f6bc77">Field of Use Restrictions</a>



<a href="https://msdn.microsoft.com/7f48967e-375a-4019-b14f-2f457b616cc0">MFT_FIELDOFUSE_UNLOCK_Attribute</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

