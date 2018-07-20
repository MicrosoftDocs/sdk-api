---
UID: NF:mfidl.IMFNetProxyLocator.RegisterProxyResult
title: IMFNetProxyLocator::RegisterProxyResult
author: windows-sdk-content
description: Keeps a record of the success or failure of using the current proxy.
old-location: mf\imfnetproxylocator_registerproxyresult.htm
old-project: medfound
ms.assetid: 2b1a55c6-7d78-47cc-9098-6504d11a4eef
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: 2b1a55c6-7d78-47cc-9098-6504d11a4eef, IMFNetProxyLocator interface [Media Foundation],RegisterProxyResult method, IMFNetProxyLocator.RegisterProxyResult, IMFNetProxyLocator::RegisterProxyResult, RegisterProxyResult, RegisterProxyResult method [Media Foundation], RegisterProxyResult method [Media Foundation],IMFNetProxyLocator interface, mf.imfnetproxylocator_registerproxyresult, mfidl/IMFNetProxyLocator::RegisterProxyResult
ms.prod: windows
ms.technology: windows-sdk
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
 - IMFNetProxyLocator.RegisterProxyResult
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFNetProxyLocator::RegisterProxyResult


## -description



Keeps a record of the success or failure of using the current proxy.




## -parameters




### -param hrOp [in]

<b>HRESULT</b> specifying the result of using the current proxy for connection.


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




<a href="https://msdn.microsoft.com/2906b998-f1ca-4c65-b810-cbc360390653">IMFNetProxyLocator</a>
 

 

