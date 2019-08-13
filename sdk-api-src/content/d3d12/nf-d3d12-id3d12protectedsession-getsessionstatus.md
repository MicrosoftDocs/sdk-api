---
UID: NF:d3d12.ID3D12ProtectedSession.GetSessionStatus
title: ID3D12ProtectedSession::GetSessionStatus (d3d12.h)
author: windows-sdk-content
description: Gets the status of the protected session.
old-location: direct3d12\id3d12protectedsession_getsessionstatus.htm
tech.root: direct3d12
ms.assetid: 9069D567-80BB-469D-A079-917D619F4F46
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSessionStatus, GetSessionStatus method, GetSessionStatus method,ID3D12ProtectedSession interface, ID3D12ProtectedSession interface,GetSessionStatus method, ID3D12ProtectedSession.GetSessionStatus, ID3D12ProtectedSession::GetSessionStatus, d3d12/ID3D12ProtectedSession::GetSessionStatus, direct3d12.id3d12protectedsession_getsessionstatus
ms.topic: method
f1_keywords: 
 - "d3d12/ID3D12ProtectedSession.GetSessionStatus"
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
ms.custom: 19H1
---

# ID3D12ProtectedSession::GetSessionStatus

## -description

Gets the status of the protected session.

## -parameters

## -returns

Type: **[D3D12_PROTECTED_SESSION_STATUS](/windows/desktop/api/d3d12/ne-d3d12-d3d12_protected_session_status)**

The status of the protected session. If the returned value is [D3D12_PROTECTED_SESSION_STATUS_INVALID](/windows/desktop/api/d3d12/ne-d3d12-d3d12_protected_session_status), then you need to wait for a uniqueness value bump to reuse the resource if the session is an [ID3D12ProtectedResourceSession](https://docs.microsoft.com/en-us/windows/desktop/api/d3d12/nn-d3d12-id3d12protectedresourcesession).

## -see-also

[ID3D12ProtectedSession](https://docs.microsoft.com/en-us/windows/desktop/api/d3d12/nn-d3d12-id3d12protectedsession)