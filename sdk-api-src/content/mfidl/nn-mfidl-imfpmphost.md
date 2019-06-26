---
UID: NN:mfidl.IMFPMPHost
title: IMFPMPHost (mfidl.h)
author: windows-sdk-content
description: Enables a media source in the application process to create objects in the protected media path (PMP) process.
old-location: mf\imfpmphost.htm
tech.root: medfound
ms.assetid: fab1fb42-07c5-4a74-b6f5-0950b2c3ba46
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFPMPHost, IMFPMPHost interface [Media Foundation], IMFPMPHost interface [Media Foundation],described, fab1fb42-07c5-4a74-b6f5-0950b2c3ba46, mf.imfpmphost, mfidl/IMFPMPHost
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFPMPHost"
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
 - IMFPMPHost
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMPHost interface


## -description


Enables a media source in the application process to create objects in the protected media path (PMP) process.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPMPHost</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFPMPHost</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPMPHost</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid">CreateObjectByCLSID</a>
</td>
<td align="left" width="63%">
Creates an object in the PMP process, from a CLSID.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-lockprocess">LockProcess</a>
</td>
<td align="left" width="63%">
Blocks the PMP process from ending.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfpmphost-remotecreateobjectbyclsid">RemoteCreateObjectByCLSID</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid">CreateObjectByCLSID</a>. (Not used by applications.)
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-unlockprocess">UnlockProcess</a>
</td>
<td align="left" width="63%">
Decrements the lock count on the PMP process.
        

</td>
</tr>
</table> 


## -remarks



This interface is used when a media source resides in the application process but the Media Session resides in a PMP process. The media source can use this interface to create objects in the PMP process. For example, to play DRM-protected content, the media source typically must create an input trust authority (ITA) in the PMP process. 

To use this interface, the media source implements the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient">IMFPMPClient</a> interface. The PMP Media Session calls <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpmpclient-setpmphost">IMFPMPClient::SetPMPHost</a> on the media source, passing in a pointer to the <b>IMFPMPHost</b> interface.

You can also get a pointer to this interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> on the PMP Media Session, using the service identifier <b>MF_PMP_SERVICE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/pmp-media-session">PMP Media Session</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/protected-media-path">Protected Media Path</a>
 

 

