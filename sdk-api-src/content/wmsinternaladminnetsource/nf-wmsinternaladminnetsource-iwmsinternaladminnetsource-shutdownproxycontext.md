---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource.ShutdownProxyContext
title: IWMSInternalAdminNetSource::ShutdownProxyContext
author: windows-sdk-content
description: The ShutdownProxyContext method releases the internal resources used by IWMSInternalAdminNetSource::FindProxyForURL. To avoid memory leaks, you must call this method after you are finished making calls to FindProxyForURL.
old-location: wmformat\iwmsinternaladminnetsource_shutdownproxycontext.htm
tech.root: wmformat
ms.assetid: 95c6f641-e0b1-4391-b4bd-b43c03a330b4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMSInternalAdminNetSource interface [windows Media Format],ShutdownProxyContext method, IWMSInternalAdminNetSource.ShutdownProxyContext, IWMSInternalAdminNetSource::ShutdownProxyContext, IWMSInternalAdminNetSourceShutdownProxyContext, ShutdownProxyContext, ShutdownProxyContext method [windows Media Format], ShutdownProxyContext method [windows Media Format],IWMSInternalAdminNetSource interface, wmformat.iwmsinternaladminnetsource_shutdownproxycontext, wmsinternaladminnetsource/IWMSInternalAdminNetSource::ShutdownProxyContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsinternaladminnetsource.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMSInternalAdminNetSource.ShutdownProxyContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmsinternaladminnetsource.h
: 
- IWMSInternalAdminNetSource.ShutdownProxyContext
: 
---

# IWMSInternalAdminNetSource::ShutdownProxyContext


## -description



The <b>ShutdownProxyContext</b> method releases the internal resources used by <a href="https://msdn.microsoft.com/5c05ed2b-98ff-417c-bc48-4e8a3dd95460">IWMSInternalAdminNetSource::FindProxyForURL</a>. To avoid memory leaks, you must call this method after you are finished making calls to <b>FindProxyForURL</b>.




## -parameters




### -param dwProxyContext [in]

<b>DWORD</b> containing the proxy context. Set this to the last proxy context received from <b>FindProxyForURL</b>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0fbdad85-d94a-4598-bb25-f733df33692a">IWMSInternalAdminNetSource Interface</a>
 

 

