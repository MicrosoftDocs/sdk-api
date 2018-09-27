---
UID: NN:mfmediaengine.IMFMediaEngineProtectedContent
title: IMFMediaEngineProtectedContent
author: windows-sdk-content
description: Enables the Media Engine to play protected video content.
old-location: mf\imfmediaengineprotectedcontent.htm
tech.root: medfound
ms.assetid: 85B37711-DB46-4BC7-A051-79E9507791FA
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IMFMediaEngineProtectedContent, IMFMediaEngineProtectedContent interface [Media Foundation], IMFMediaEngineProtectedContent interface [Media Foundation],described, mf.imfmediaengineprotectedcontent, mfmediaengine/IMFMediaEngineProtectedContent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfmediaengine.h
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
 - mfmediaengine.h
api_name:
 - IMFMediaEngineProtectedContent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineProtectedContent interface


## -description


Enables the Media Engine to play protected video content.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineProtectedContent</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaEngineProtectedContent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineProtectedContent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4D67813D-F222-4EB1-B059-6DB5EC642DA2">GetRequiredProtections</a>
</td>
<td align="left" width="63%">
Gets the content protections that must be applied in frame-server mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2D1F31B1-9A4E-4B94-93FF-255B3006C904">SetApplicationCertificate</a>
</td>
<td align="left" width="63%">
Sets the application's certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8F150CB5-43AB-4709-A254-636440113642">SetContentProtectionManager</a>
</td>
<td align="left" width="63%">
Sets the content protection manager (CPM).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0102A98E-5EE0-4FBE-AF82-97C7A25038FB">SetOPMWindow</a>
</td>
<td align="left" width="63%">
Specifies the window that should receive output link protections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7C94AEA2-1D72-4C45-9EDF-90593CC60E2C">ShareResources</a>
</td>
<td align="left" width="63%">
Enables the Media Engine to access protected content while in frame-server mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3A5C6908-65F4-4E7A-AD71-BBD1C2A4ACE3">TransferVideoFrame</a>
</td>
<td align="left" width="63%">
Copies a protected video frame to a DXGI surface.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the Media Engine.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

