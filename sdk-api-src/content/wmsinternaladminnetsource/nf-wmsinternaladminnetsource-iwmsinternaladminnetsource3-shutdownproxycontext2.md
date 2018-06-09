---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource3.ShutdownProxyContext2
title: IWMSInternalAdminNetSource3::ShutdownProxyContext2
author: windows-sdk-content
description: The ShutdownProxyContext2 method releases the internal resources used by IWMSInternalAdminNetSource3::FindProxyForURLEx2. To avoid memory leaks, you must call this method after you are finished making calls to FindProxyForURLEx2.
old-location: wmformat\iwmsinternaladminnetsource3_shutdownproxycontext2.htm
old-project: wmformat
ms.assetid: 83f4f504-6447-4792-9fc2-1bf479f1e6a2
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IWMSInternalAdminNetSource3 interface [windows Media Format],ShutdownProxyContext2 method, IWMSInternalAdminNetSource3.ShutdownProxyContext2, IWMSInternalAdminNetSource3::ShutdownProxyContext2, IWMSInternalAdminNetSource3ShutdownProxyContext2, ShutdownProxyContext2, ShutdownProxyContext2 method [windows Media Format], ShutdownProxyContext2 method [windows Media Format],IWMSInternalAdminNetSource3 interface, wmformat.iwmsinternaladminnetsource3_shutdownproxycontext2, wmsinternaladminnetsource/IWMSInternalAdminNetSource3::ShutdownProxyContext2
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: NETSOURCE_URLCREDPOLICY_SETTINGS
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
 - IWMSInternalAdminNetSource3.ShutdownProxyContext2
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSInternalAdminNetSource3::ShutdownProxyContext2


## -description



The <b>ShutdownProxyContext2</b> method releases the internal resources used by <a href="https://msdn.microsoft.com/03c52ed2-bf77-4013-89d6-544d048f1056">IWMSInternalAdminNetSource3::FindProxyForURLEx2</a>. To avoid memory leaks, you must call this method after you are finished making calls to <b>FindProxyForURLEx2</b>.




## -parameters




### -param qwProxyContext [in]

<b>QWORD</b> containing the proxy context. Set this to the last proxy context received from <b>FindProxyForURLEx2</b>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b4ca08a4-6e2d-4646-b101-67bac67300b1">IWMSInternalAdminNetSource3 Interface</a>
 

 

