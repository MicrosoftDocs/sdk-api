---
UID: NF:wsmandisp.IWSManEx.CreateResourceLocator
title: IWSManEx::CreateResourceLocator (wsmandisp.h)
author: windows-sdk-content
description: Creates a ResourceLocator object that can be used instead of a resource URI in Session object operations such as IWSManSession.Get, IWSManSession.Put, or Session.Enumerate.
old-location: winrm\iwsmanex_createresourcelocator.htm
tech.root: winrm
ms.assetid: b670865d-96d6-4b06-a9a5-ed74574a0108
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateResourceLocator, CreateResourceLocator method [Windows Remote Management], CreateResourceLocator method [Windows Remote Management],IWSManEx interface, IWSManEx interface [Windows Remote Management],CreateResourceLocator method, IWSManEx.CreateResourceLocator, IWSManEx::CreateResourceLocator, winrm.iwsmanex_createresourcelocator, wsmandisp/IWSManEx::CreateResourceLocator
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
 - IWSManEx.CreateResourceLocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSManEx::CreateResourceLocator


## -description


Creates a <a href="https://docs.microsoft.com/windows/desktop/WinRM/resourcelocator">ResourceLocator</a> object that can be used instead of a resource URI in <a href="https://docs.microsoft.com/windows/desktop/WinRM/session">Session</a> object operations such as <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-get">IWSManSession.Get</a>, <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-put">IWSManSession.Put</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">Session.Enumerate</a>.


## -parameters




### -param strResourceLocator [in]

The resource URI for the resource. For more information about URI strings, see <a href="https://docs.microsoft.com/windows/desktop/WinRM/resource-uris">Resource URIs</a>.


### -param newResourceLocator [out]

A pointer to a new instance of <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <b>FragmentDialect</b> property is not specified in the <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a> object, the default is the XPath 1.0 specification. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84163">http://www.w3.org/TR/xpath</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex">IWSManEx</a>



<a href="https://docs.microsoft.com/windows/desktop/WinRM/wsman">WSMan</a>



<a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-reference">Windows Remote Management Reference</a>
 

 

