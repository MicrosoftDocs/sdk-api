---
UID: NF:mbnapi.IMbnInterface.GetConnection
title: IMbnInterface::GetConnection (mbnapi.h)
author: windows-sdk-content
description: Gets the IMbnConnection object.
old-location: mbn\imbninterface_getconnection.htm
tech.root: mbn
ms.assetid: 919772f5-1e86-424c-b3de-079a03bbc8e5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetConnection, GetConnection method [Microsoft Broadband Networks], GetConnection method [Microsoft Broadband Networks],IMbnInterface interface, IMbnInterface interface [Microsoft Broadband Networks],GetConnection method, IMbnInterface.GetConnection, IMbnInterface::GetConnection, mbn.imbninterface_getconnection, mbnapi/IMbnInterface::GetConnection
ms.topic: method
f1_keywords: 
 - "mbnapi/IMbnInterface.GetConnection"
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - mbnapi.h
api_name:
 - IMbnInterface.GetConnection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnInterface::GetConnection


## -description


Gets the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> object associated with this interface.


## -parameters




### -param mbnConnection [out]

The <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> object.


## -returns



This method can return one of these values.

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
The method completed successfully.  <i>mbnConnection</i> contains a valid object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
Either there is no available connection or the device is not registered to a network.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>
 

 

