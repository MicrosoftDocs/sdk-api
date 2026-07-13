---
UID: NF:wsmandisp.IWSManSession.Put
title: IWSManSession::Put (wsmandisp.h)
description: Updates a resource.
helpviewer_keywords: ["IWSManSession interface [Windows Remote Management]","Put method","IWSManSession.Put","IWSManSession::Put","Put","Put method [Windows Remote Management]","Put method [Windows Remote Management]","IWSManSession interface","winrm.iwsmansession_put","wsmandisp/IWSManSession::Put"]
old-location: winrm\iwsmansession_put.htm
tech.root: winrm
ms.assetid: 1224dab8-82d1-4416-8c21-e84fdda15deb
ms.date: 12/05/2018
ms.keywords: IWSManSession interface [Windows Remote Management],Put method, IWSManSession.Put, IWSManSession::Put, Put, Put method [Windows Remote Management], Put method [Windows Remote Management],IWSManSession interface, winrm.iwsmansession_put, wsmandisp/IWSManSession::Put
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSManSession::Put
 - wsmandisp/IWSManSession::Put
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManSession.Put
---

# IWSManSession::Put


## -description

Updates a resource.

## -parameters

### -param resourceUri [in]

The identifier of the resource to be updated.

This parameter can contain one of the following:

<ul>
<li>URI with or without <a href="/windows/desktop/WinRM/windows-remote-management-glossary">selectors</a>. When calling the <b>Put</b> method to obtain a WMI resource, use the key property or properties of the object.</li>
<li>
<a href="/windows/desktop/WinRM/resourcelocator">ResourceLocator</a> object which may contain selectors,  <a href="/windows/desktop/WinRM/windows-remote-management-glossary">fragments</a>, or <a href="/windows/desktop/WinRM/windows-remote-management-glossary">options</a>.</li>
<li><a href="/windows/desktop/WinRM/windows-remote-management-glossary">WS-Addressing</a> endpoint reference as described in the WS-Management protocol  standard.  For more information about the public specification for the WS-Management protocol, see <a href="/previous-versions/dotnet/articles/ms951267(v=msdn.10)">Management Specifications Index Page</a>.</li>
</ul>

### -param resource [in]

The updated resource content.

### -param flags [in]

Reserved for future use. Must be set to 0.

### -param resultResource [out]

The XML stream that contains the updated resource content.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a>



<a href="/windows/desktop/WinRM/session-put">Session.Put</a>