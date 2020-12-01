---
UID: NF:pla.IDataCollectorSet.get_UserAccount
title: IDataCollectorSet::get_UserAccount (pla.h)
description: Retrieves the user account under which the data collector set will run.
helpviewer_keywords: ["IDataCollectorSet interface [PLA]","UserAccount property","IDataCollectorSet.UserAccount","IDataCollectorSet.get_UserAccount","IDataCollectorSet::UserAccount","IDataCollectorSet::get_UserAccount","UserAccount property [PLA]","UserAccount property [PLA]","IDataCollectorSet interface","base.idatacollectorset_get_useraccount","get_UserAccount","pla.idatacollectorset_get_useraccount","pla/IDataCollectorSet::UserAccount","pla/IDataCollectorSet::get_UserAccount"]
old-location: pla\idatacollectorset_get_useraccount.htm
tech.root: PLA
ms.assetid: 32fe1dcf-9682-40fd-b301-45385fa33cbe
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],UserAccount property, IDataCollectorSet.UserAccount, IDataCollectorSet.get_UserAccount, IDataCollectorSet::UserAccount, IDataCollectorSet::get_UserAccount, UserAccount property [PLA], UserAccount property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_useraccount, get_UserAccount, pla.idatacollectorset_get_useraccount, pla/IDataCollectorSet::UserAccount, pla/IDataCollectorSet::get_UserAccount
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDataCollectorSet::get_UserAccount
 - pla/IDataCollectorSet::get_UserAccount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSet.UserAccount
 - IDataCollectorSet.get_UserAccount
---

# IDataCollectorSet::get_UserAccount


## -description

Retrieves the user account under which the data collector set will run.

This property is read-only.

## -parameters

## -remarks

The user name is set using the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-setcredentials">IDataCollectorSet::SetCredentials</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-setcredentials">IDataCollectorSet::SetCredentials</a>