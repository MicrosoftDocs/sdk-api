---
UID: NF:pla.IDataCollectorSet.SetCredentials
title: IDataCollectorSet::SetCredentials (pla.h)
description: Specifies the user account under which the data collector set runs.
helpviewer_keywords: ["IDataCollectorSet interface [PLA]","SetCredentials method","IDataCollectorSet.SetCredentials","IDataCollectorSet::SetCredentials","SetCredentials","SetCredentials method [PLA]","SetCredentials method [PLA]","IDataCollectorSet interface","base.idatacollectorset_setcredentials","pla.idatacollectorset_setcredentials","pla/IDataCollectorSet::SetCredentials"]
old-location: pla\idatacollectorset_setcredentials.htm
tech.root: PLA
ms.assetid: 39275154-fe85-492e-9d64-79d17cb4f88d
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],SetCredentials method, IDataCollectorSet.SetCredentials, IDataCollectorSet::SetCredentials, SetCredentials, SetCredentials method [PLA], SetCredentials method [PLA],IDataCollectorSet interface, base.idatacollectorset_setcredentials, pla.idatacollectorset_setcredentials, pla/IDataCollectorSet::SetCredentials
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
 - IDataCollectorSet::SetCredentials
 - pla/IDataCollectorSet::SetCredentials
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
 - IDataCollectorSet.SetCredentials
---

# IDataCollectorSet::SetCredentials


## -description

Specifies the user account under which the data collector set runs.

## -parameters

### -param user [in]

A user account under which the data collector set runs. Specify the user name in the form <i>domain</i>&#92;<i>user</i> or <i>user</i>@<i>domain</i>.

### -param password [in]

The password of the user account.

## -returns

The property returns S_OK if successful.

## -remarks

To clear the user credentials, set both parameters to <b>NULL</b>.

If you do not specify the credentials, PLA tries to run the set as LocalSystem if the current user is a member of the administrator group.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_useraccount">IDataCollectorSet::UserAccount</a>