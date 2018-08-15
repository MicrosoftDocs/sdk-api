---
UID: NN:mfidl.IMFPMPServer
title: IMFPMPServer
author: windows-sdk-content
description: Enables two instances of the Media Session to share the same protected media path (PMP) process.
old-location: mf\imfpmpserver.htm
old-project: medfound
ms.assetid: ba6dc70a-d77d-41de-afe1-65f2efcc4a95
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFPMPServer, IMFPMPServer interface [Media Foundation], IMFPMPServer interface [Media Foundation],described, ba6dc70a-d77d-41de-afe1-65f2efcc4a95, mf.imfpmpserver, mfidl/IMFPMPServer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFPMPServer
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMPServer interface


## -description


Enables two instances of the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> to share the same protected media path (PMP) process.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPMPServer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFPMPServer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPMPServer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ece956bb-ee83-42c7-9410-90f34956fdde">CreateObjectByCLSID</a>
</td>
<td align="left" width="63%">
Creates an object in the PMP process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a25abfb-5038-4869-ad70-1ae52e8cf599">LockProcess</a>
</td>
<td align="left" width="63%">
Blocks the PMP process from ending.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f64252f-c08b-4624-8df6-db922a630891">UnlockProcess</a>
</td>
<td align="left" width="63%">
Decrements the lock count on the PMP process.

</td>
</tr>
</table> 


## -remarks



If your application creates more than one instance of the Media Session, you can use this interface to share the same PMP process among several instances. This can be more efficient than re-creating the PMP process each time.

Use this interface as follows:

<ol>
<li>Create the first instance of the PMP Media Session by calling <a href="https://msdn.microsoft.com/cb492e68-3d8a-49b2-8c0b-bee8065b53a8">MFCreatePMPMediaSession</a>.
          </li>
<li>Retrieve an <b>IMFPMPServer</b> pointer from the first Media Session by calling <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> with the service identifier <b>MF_PMP_SERVER_CONTEXT</b>.
          </li>
<li>Create the second instance of the PMP Media Session. Set the <a href="https://msdn.microsoft.com/a922c79b-d6c1-447d-b6fa-993970169a3f">MF_SESSION_SERVER_CONTEXT</a> attribute on the <i>pConfiguration</i> parameter of the <a href="https://msdn.microsoft.com/cb492e68-3d8a-49b2-8c0b-bee8065b53a8">MFCreatePMPMediaSession</a> function. The attribute value is the <b>IMFPMPServer</b> pointer retrieved in step 2.
          </li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/CF3A427D-31D2-45FF-BE87-F192B758204E">PMP Media Session</a>
 

 

