---
UID: NN:mfidl.IMFPMPHost
title: IMFPMPHost
author: windows-sdk-content
description: Enables a media source in the application process to create objects in the protected media path (PMP) process.
old-location: mf\imfpmphost.htm
tech.root: medfound
ms.assetid: fab1fb42-07c5-4a74-b6f5-0950b2c3ba46
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFPMPHost, IMFPMPHost interface [Media Foundation], IMFPMPHost interface [Media Foundation],described, fab1fb42-07c5-4a74-b6f5-0950b2c3ba46, mf.imfpmphost, mfidl/IMFPMPHost
ms.prod: windows
ms.technology: windows-sdk
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
 - IMFPMPHost
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMPHost interface


## -description


Enables a media source in the application process to create objects in the protected media path (PMP) process.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPMPHost</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFPMPHost</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/787fc392-1858-41f4-a1ce-2da02a5e789f">CreateObjectByCLSID</a>
</td>
<td align="left" width="63%">
Creates an object in the PMP process, from a CLSID.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45c533ca-d8ca-43f9-91d2-011a0b0d63a6">LockProcess</a>
</td>
<td align="left" width="63%">
Blocks the PMP process from ending.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be96be6d-47de-4d2b-81fc-13079de33888">RemoteCreateObjectByCLSID</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/787fc392-1858-41f4-a1ce-2da02a5e789f">CreateObjectByCLSID</a>. (Not used by applications.)
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/768f4579-5109-4d2b-a93d-f17f6b850c63">UnlockProcess</a>
</td>
<td align="left" width="63%">
Decrements the lock count on the PMP process.
        

</td>
</tr>
</table> 


## -remarks



This interface is used when a media source resides in the application process but the Media Session resides in a PMP process. The media source can use this interface to create objects in the PMP process. For example, to play DRM-protected content, the media source typically must create an input trust authority (ITA) in the PMP process. 

To use this interface, the media source implements the <a href="https://msdn.microsoft.com/adfba5dd-eae6-48f3-a155-65bd491c952c">IMFPMPClient</a> interface. The PMP Media Session calls <a href="https://msdn.microsoft.com/d6e48f36-7896-4e6d-ba10-d8c0288ccffc">IMFPMPClient::SetPMPHost</a> on the media source, passing in a pointer to the <b>IMFPMPHost</b> interface.

You can also get a pointer to this interface by calling <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> on the PMP Media Session, using the service identifier <b>MF_PMP_SERVICE</b>.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/CF3A427D-31D2-45FF-BE87-F192B758204E">PMP Media Session</a>



<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
 

 

