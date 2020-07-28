---
UID: NF:wmsdkidl.IWMClientConnections2.GetClientInfo
title: IWMClientConnections2::GetClientInfo (wmsdkidl.h)
description: The GetClientInfo method retrieves information about a client attached to a writer network sink.
helpviewer_keywords: ["GetClientInfo","GetClientInfo method [windows Media Format]","GetClientInfo method [windows Media Format]","IWMClientConnections2 interface","IWMClientConnections2 interface [windows Media Format]","GetClientInfo method","IWMClientConnections2.GetClientInfo","IWMClientConnections2::GetClientInfo","IWMClientConnections2GetClientInfo","wmformat.iwmclientconnections2_getclientinfo","wmsdkidl/IWMClientConnections2::GetClientInfo"]
old-location: wmformat\iwmclientconnections2_getclientinfo.htm
tech.root: wmformat
ms.assetid: 39731e6a-cfd7-48c5-9107-bf5373dfeb4a
ms.date: 12/05/2018
ms.keywords: GetClientInfo, GetClientInfo method [windows Media Format], GetClientInfo method [windows Media Format],IWMClientConnections2 interface, IWMClientConnections2 interface [windows Media Format],GetClientInfo method, IWMClientConnections2.GetClientInfo, IWMClientConnections2::GetClientInfo, IWMClientConnections2GetClientInfo, wmformat.iwmclientconnections2_getclientinfo, wmsdkidl/IWMClientConnections2::GetClientInfo
f1_keywords:
- wmsdkidl/IWMClientConnections2.GetClientInfo
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
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
- IWMClientConnections2.GetClientInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMClientConnections2::GetClientInfo


## -description



The <b>GetClientInfo</b> method retrieves information about a client attached to a writer network sink.




## -parameters




### -param dwClientNum [in]

<b>DWORD</b> containing the client number.


### -param pwszNetworkAddress [out]

Pointer to a wide-character <b>null</b>-terminated string containing the network address of the client. Pass <b>NULL</b> to retrieve the size of the string, which is returned in <i>pcchNetworkAddress</i>.


### -param pcchNetworkAddress [in, out]

Pointer to a <b>DWORD</b> containing the size of <i>pwszNetworkAddress</i>, in wide characters. This size includes the terminating <b>null</b> character.


### -param pwszPort [out]

Pointer to a wide-character <b>null</b>-terminated string containing the network port of the client. Pass <b>NULL</b> to retrieve the size of the string, which is returned in <i>pcchPort</i>.


### -param pcchPort [in, out]

Pointer to a <b>DWORD</b> containing the size of <i>pwszPort</i>, in wide characters. This size includes the terminating <b>null</b> character.


### -param pwszDNSName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the name of the domain name server supporting the client. Pass <b>NULL</b> to retrieve the size of the string, which is returned in <i>pcchDNSName</i>.


### -param pcchDNSName [in, out]

Pointer to a <b>DWORD</b> containing the size of <i>pwszDNSName</i>, in wide characters. This size includes the terminating <b>null</b> character.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2">IWMClientConnections2 Interface</a>
 

 

