---
UID: NF:mfidl.IMFPMPServer.CreateObjectByCLSID
title: IMFPMPServer::CreateObjectByCLSID
author: windows-sdk-content
description: Creates an object in the protected media path (PMP) process.
old-location: mf\imfpmpserver_createobjectbyclsid.htm
tech.root: medfound
ms.assetid: ece956bb-ee83-42c7-9410-90f34956fdde
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CreateObjectByCLSID, CreateObjectByCLSID method [Media Foundation], CreateObjectByCLSID method [Media Foundation],IMFPMPServer interface, IMFPMPServer interface [Media Foundation],CreateObjectByCLSID method, IMFPMPServer.CreateObjectByCLSID, IMFPMPServer::CreateObjectByCLSID, ece956bb-ee83-42c7-9410-90f34956fdde, mf.imfpmpserver_createobjectbyclsid, mfidl/IMFPMPServer::CreateObjectByCLSID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMFPMPServer.CreateObjectByCLSID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMPServer::CreateObjectByCLSID


## -description



Creates an object in the protected media path (PMP) process.




## -parameters




### -param clsid [in]

CLSID of the object to create.


### -param riid [in]

Interface identifier of the interface to retrieve.


### -param ppObject [out]

Receives a pointer to the requested interface. The caller must release the interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ba6dc70a-d77d-41de-afe1-65f2efcc4a95">IMFPMPServer</a>
 

 

