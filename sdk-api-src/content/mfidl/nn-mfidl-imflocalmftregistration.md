---
UID: NN:mfidl.IMFLocalMFTRegistration
title: IMFLocalMFTRegistration
author: windows-sdk-content
description: Registers Media Foundation transforms (MFTs) in the caller's process.
old-location: mf\imflocalmftregistration.htm
tech.root: medfound
ms.assetid: e540a93a-ecce-4c5b-a121-b0f868a2af41
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFLocalMFTRegistration, IMFLocalMFTRegistration interface [Media Foundation], IMFLocalMFTRegistration interface [Media Foundation],described, mf.imflocalmftregistration, mfidl/IMFLocalMFTRegistration
ms.prod: windows
ms.technology: windows-sdk
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
 - IMFLocalMFTRegistration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFLocalMFTRegistration interface


## -description


Registers Media Foundation transforms (MFTs) in the caller's process.

The Media Session exposes this interface as a service. To obtain a pointer to this interface, call the <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> method on the Media Session with the service identifier <b>MF_LOCAL_MFT_REGISTRATION_SERVICE</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFLocalMFTRegistration</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFLocalMFTRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFLocalMFTRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f77b5b9-94af-42b1-83ca-cb3310083632">RegisterMFTs</a>
</td>
<td align="left" width="63%">
Registers one or more  MFTs in the caller's process.

</td>
</tr>
</table> 


## -remarks



This interface requires the Media Session. If you are not using the Media Session for playback, call one of the following functions instead:

<ul>
<li>
<a href="https://msdn.microsoft.com/802f7083-e224-4e5c-8a35-3e93da0cbd91">MFTRegisterLocal</a>
</li>
<li>
<a href="https://msdn.microsoft.com/80c45ac3-4487-41bf-a5f5-f459db3cd700">MFTRegisterLocalByCLSID</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

