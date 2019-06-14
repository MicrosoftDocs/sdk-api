---
UID: NF:wsmandisp.IWSManSession.Get
title: IWSManSession::Get (wsmandisp.h)
author: windows-sdk-content
description: Retrieves the resource specified by the URI and returns an XML representation of the current instance of the resource.
old-location: winrm\iwsmansession_get.htm
tech.root: winrm
ms.assetid: f6393cfb-0787-4d30-8d02-be0996885f22
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Get, Get method [Windows Remote Management], Get method [Windows Remote Management],IWSManSession interface, IWSManSession interface [Windows Remote Management],Get method, IWSManSession.Get, IWSManSession::Get, winrm.iwsmansession_get, wsmandisp/IWSManSession::Get
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManSession.Get
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSManSession::Get


## -description


Retrieves the resource specified by the  <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">URI</a> and returns an XML representation of the current instance of the resource.


## -parameters




### -param resourceUri [in]

The identifier of the resource to be retrieved.

This parameter can contain one of the following:

<ul>
<li>URI with or without  <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">selectors</a>. When calling the <a href="https://docs.microsoft.com/windows/desktop/WinRM/session-get">Get</a> method to obtain a WMI resource, use the key property or properties of the object.</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/WinRM/resourcelocator">ResourceLocator</a> object which may contain selectors,  <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">fragments</a>, or <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">options</a>.</li>
<li><a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">WS-Addressing</a> endpoint reference as described in the WS-Management protocol  standard.  For more information about the public specification for the WS-Management protocol, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84316">Management Specifications Index Page</a>.</li>
</ul>

### -param flags [in]

Reserved for future use. Must be set to 0.


### -param resource [out]

A value that, upon success, is an XML representation of the resource.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a>



<a href="https://docs.microsoft.com/windows/desktop/WinRM/session-get">Session.Get</a>
 

 

