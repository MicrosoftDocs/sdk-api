---
UID: NF:mfidl.IMFByteStreamCacheControl.StopBackgroundTransfer
title: IMFByteStreamCacheControl::StopBackgroundTransfer
author: windows-sdk-content
description: Stops the background transfer of data to the local cache.
old-location: mf\imfbytestreamcachecontrol_stopbackgroundtransfer.htm
old-project: medfound
ms.assetid: 9f0f7102-c839-4e92-a798-5ea31ceba013
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFByteStreamCacheControl interface [Media Foundation],StopBackgroundTransfer method, IMFByteStreamCacheControl.StopBackgroundTransfer, IMFByteStreamCacheControl::StopBackgroundTransfer, StopBackgroundTransfer, StopBackgroundTransfer method [Media Foundation], StopBackgroundTransfer method [Media Foundation],IMFByteStreamCacheControl interface, mf.imfbytestreamcachecontrol_stopbackgroundtransfer, mfidl/IMFByteStreamCacheControl::StopBackgroundTransfer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - mfidl.h
api_name:
 - IMFByteStreamCacheControl.StopBackgroundTransfer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFByteStreamCacheControl::StopBackgroundTransfer


## -description


Stops the background transfer of data to the local cache.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The byte stream resumes transferring data to the cache if the application does one of the following:

<ul>
<li>Reads data from the byte stream.</li>
<li>Calls the byte stream's <a href="https://msdn.microsoft.com/5f7418ff-32e5-49b3-b7b3-6686e6562d51">IMFByteStreamBuffering::EnableBuffering</a> method.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/e12a532a-4624-4e06-8e19-6e9daec550ac">IMFByteStreamCacheControl</a>
 

 

