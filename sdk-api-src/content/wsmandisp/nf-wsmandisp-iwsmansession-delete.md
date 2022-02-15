---
UID: NF:wsmandisp.IWSManSession.Delete
title: IWSManSession::Delete (wsmandisp.h)
description: Deletes the resource specified in the resource URI.
helpviewer_keywords: ["Delete","Delete method [Windows Remote Management]","Delete method [Windows Remote Management]","IWSManSession interface","IWSManSession interface [Windows Remote Management]","Delete method","IWSManSession.Delete","IWSManSession::Delete","winrm.iwsmansession_delete","wsmandisp/IWSManSession::Delete"]
old-location: winrm\iwsmansession_delete.htm
tech.root: winrm
ms.assetid: 63674a3a-4819-4695-a8f5-648787d78cc4
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Windows Remote Management], Delete method [Windows Remote Management],IWSManSession interface, IWSManSession interface [Windows Remote Management],Delete method, IWSManSession.Delete, IWSManSession::Delete, winrm.iwsmansession_delete, wsmandisp/IWSManSession::Delete
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
 - IWSManSession::Delete
 - wsmandisp/IWSManSession::Delete
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
 - IWSManSession.Delete
---

# IWSManSession::Delete


## -description

Deletes the resource specified in the resource URI.

## -parameters

### -param resourceUri [in]

The URI of the resource to be deleted. You can also use an <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a> object to specify the resource.

### -param flags [in, optional]

Reserved for future use. Must be set to 0.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a>



<a href="/windows/desktop/WinRM/session-delete">Session.Delete</a>