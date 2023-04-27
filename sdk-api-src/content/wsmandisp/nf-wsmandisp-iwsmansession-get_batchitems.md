---
UID: NF:wsmandisp.IWSManSession.get_BatchItems
title: IWSManSession::get_BatchItems (wsmandisp.h)
description: Sets and gets the number of items in each enumeration batch. (Get)
helpviewer_keywords: ["BatchItems property [Windows Remote Management]","BatchItems property [Windows Remote Management]","IWSManSession interface","IWSManSession interface [Windows Remote Management]","BatchItems property","IWSManSession.BatchItems","IWSManSession.get_BatchItems","IWSManSession::BatchItems","IWSManSession::get_BatchItems","IWSManSession::put_BatchItems","get_BatchItems","winrm.iwsmansession_batchitems","wsmandisp/IWSManSession::BatchItems","wsmandisp/IWSManSession::get_BatchItems","wsmandisp/IWSManSession::put_BatchItems"]
old-location: winrm\iwsmansession_batchitems.htm
tech.root: winrm
ms.assetid: 883fc265-b84e-4757-a9b1-8c52174cb701
ms.date: 12/05/2018
ms.keywords: BatchItems property [Windows Remote Management], BatchItems property [Windows Remote Management],IWSManSession interface, IWSManSession interface [Windows Remote Management],BatchItems property, IWSManSession.BatchItems, IWSManSession.get_BatchItems, IWSManSession::BatchItems, IWSManSession::get_BatchItems, IWSManSession::put_BatchItems, get_BatchItems, winrm.iwsmansession_batchitems, wsmandisp/IWSManSession::BatchItems, wsmandisp/IWSManSession::get_BatchItems, wsmandisp/IWSManSession::put_BatchItems
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
 - IWSManSession::get_BatchItems
 - wsmandisp/IWSManSession::get_BatchItems
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
 - IWSManSession.BatchItems
 - IWSManSession.get_BatchItems
 - IWSManSession.put_BatchItems
---

# IWSManSession::get_BatchItems


## -description

Sets and gets the number of   items in each enumeration batch. This value cannot be changed during an enumeration.  The resource provider may set a limit.

This property is read/write.

## -parameters

## -remarks

This is an optimization feature that controls how often network calls are made between the client and the server. Currently, it is used only for enumerations. For more information about enumerating resources, see  <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanenumerator">IWSManEnumerator</a>.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a>



<a href="/windows/desktop/WinRM/session-batchitems">Session.BatchItems</a>
