---
UID: NF:d3d12.ID3D12ProtectedSession.GetSessionStatus
title: ID3D12ProtectedSession::GetSessionStatus
author: windows-sdk-content
description: Gets the status of the protected session.
old-location: direct3d12\id3d12protectedsession_getsessionstatus.htm
tech.root: direct3d12
ms.assetid: 9069D567-80BB-469D-A079-917D619F4F46
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSessionStatus, GetSessionStatus method, GetSessionStatus method,ID3D12ProtectedSession interface, ID3D12ProtectedSession interface,GetSessionStatus method, ID3D12ProtectedSession.GetSessionStatus, ID3D12ProtectedSession::GetSessionStatus, d3d12/ID3D12ProtectedSession::GetSessionStatus, direct3d12.id3d12protectedsession_getsessionstatus
ms.topic: method
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12ProtectedSession.GetSessionStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12ProtectedSession::GetSessionStatus


## -description


Gets the status of the protected session.


## -parameters






## -returns



The status the protected session. If <b>D3D12_PROTECTED_SESSION_STATUS_INVALID</b>, then you need to wait for a uniqueness value bump to reuse the resource if the session is an <a href="https://msdn.microsoft.com/9D4833DB-DF9E-46A8-9EF7-667A95F3EFDD">ID3D12ProtectedResourceSession</a>. If <a href="direct3d12.id3d12cryptosession">ID3D12CryptoSession</a> or <a href="direct3d12.id3d12cryptosessionpolicy">ID3D12CryptoSessionPolicy</a>, then they need to be recreated.




## -see-also




<a href="https://msdn.microsoft.com/BBB87F18-A4F4-44E7-AFD8-803BD2C7C753">ID3D12ProtectedSession</a>
 

 

