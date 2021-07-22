---
UID: NF:wsmandisp.IWSManSession.Create
title: IWSManSession::Create (wsmandisp.h)
description: Creates a new instance of a resource and returns the endpoint reference (EPR) of the new object.
helpviewer_keywords: ["Create","Create method [Windows Remote Management]","Create method [Windows Remote Management]","IWSManSession interface","IWSManSession interface [Windows Remote Management]","Create method","IWSManSession.Create","IWSManSession::Create","winrm.iwsmansession_create","wsmandisp/IWSManSession::Create"]
old-location: winrm\iwsmansession_create.htm
tech.root: winrm
ms.assetid: 7e8b561e-c724-427b-88a0-34a6c8a9c6bd
ms.date: 12/05/2018
ms.keywords: Create, Create method [Windows Remote Management], Create method [Windows Remote Management],IWSManSession interface, IWSManSession interface [Windows Remote Management],Create method, IWSManSession.Create, IWSManSession::Create, winrm.iwsmansession_create, wsmandisp/IWSManSession::Create
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
 - IWSManSession::Create
 - wsmandisp/IWSManSession::Create
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
 - IWSManSession.Create
---

# IWSManSession::Create


## -description

Creates a new instance of a resource and returns the <a href="/windows/desktop/WinRM/windows-remote-management-glossary">endpoint reference</a> (EPR) of the new object.

## -parameters

### -param resourceUri [in]

The identifier of the resource to create.

This parameter can contain one of the following:

<ul>
<li>URI with one or more  <a href="/windows/desktop/WinRM/windows-remote-management-glossary">selectors</a>. Be aware that the <a href="/windows/desktop/WinRM/windows-remote-management-glossary">WMI plug-in</a> does not support creating any resource other than a WS-Management protocol listener.</li>
<li>
<a href="/windows/desktop/WinRM/resourcelocator">ResourceLocator</a> object which may contain selectors,  <a href="/windows/desktop/WinRM/windows-remote-management-glossary">fragments</a>, or <a href="/windows/desktop/WinRM/windows-remote-management-glossary">options</a>.</li>
<li><a href="/windows/desktop/WinRM/windows-remote-management-glossary">WS-Addressing</a> endpoint reference as described in the WS-Management protocol  standard.  For more information about the public specification for the WS-Management protocol, see  <a href="/previous-versions/dotnet/articles/ms951267(v=msdn.10)">Management Specifications Index Page</a>.</li>
</ul>

### -param resource [in]

An XML string that contains resource content.

### -param flags [in]

Reserved. Must be set to 0.

### -param newUri [out]

The EPR of the new resource.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IWSManSession::Create</b> is only used for creating new 
    instances of a resource. Use the <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-put">IWSManSession::Put</a> method to 
    update existing instances of a resource. After you obtain the new resource URI, you can call 
    <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-get">IWSManSession::Get</a> to retrieve the new object. The new object 
    contains any properties that the resource provider assigns when creating the new object. For example, if you 
    create a new WS-Management protocol<a href="/windows/desktop/WinRM/windows-remote-management-glossary">listener</a> and retrieve the listener object using <a href="/windows/desktop/WinRM/session-get">Session.Get</a>, then you also obtain the <b>Port</b>, <b>Enabled</b>, and <b>ListeningOn</b> properties.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a>



<a href="/windows/desktop/WinRM/session-create">Session.Create</a>