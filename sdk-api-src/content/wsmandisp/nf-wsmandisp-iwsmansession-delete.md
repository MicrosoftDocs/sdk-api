---
UID: NF:wsmandisp.IWSManSession.Delete
title: IWSManSession::Delete (wsmandisp.h)
author: windows-sdk-content
description: Deletes the resource specified in the resource URI.
old-location: winrm\iwsmansession_delete.htm
tech.root: winrm
ms.assetid: 63674a3a-4819-4695-a8f5-648787d78cc4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Windows Remote Management], Delete method [Windows Remote Management],IWSManSession interface, IWSManSession interface [Windows Remote Management],Delete method, IWSManSession.Delete, IWSManSession::Delete, winrm.iwsmansession_delete, wsmandisp/IWSManSession::Delete
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
 - IWSManSession.Delete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSManSession::Delete


## -description


Deletes the resource specified in the resource URI.


## -parameters




### -param resourceUri [in]

The URI of the resource to be deleted. You can also use an <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a> object to specify the resource.


### -param flags [in, optional]

Reserved for future use. Must be set to 0.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a>



<a href="https://docs.microsoft.com/windows/desktop/WinRM/session-delete">Session.Delete</a>
 

 

