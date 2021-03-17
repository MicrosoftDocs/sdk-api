---
UID: NF:objsel.IDsObjectPickerCredentials.SetCredentials
title: IDsObjectPickerCredentials::SetCredentials (objsel.h)
description: Use this method to override the user credentials, passing new credentials for the account profile to be used.
helpviewer_keywords: ["IDsObjectPickerCredentials interface [Active Directory]","SetCredentials method","IDsObjectPickerCredentials.SetCredentials","IDsObjectPickerCredentials::SetCredentials","SetCredentials","SetCredentials method [Active Directory]","SetCredentials method [Active Directory]","IDsObjectPickerCredentials interface","ad.idsobjectpickercredentials_setcredentials","objsel/IDsObjectPickerCredentials::SetCredentials"]
old-location: ad\idsobjectpickercredentials_setcredentials.htm
tech.root: ad
ms.assetid: fb1c366d-10df-4e4f-a381-3f085bd136e2
ms.date: 12/05/2018
ms.keywords: IDsObjectPickerCredentials interface [Active Directory],SetCredentials method, IDsObjectPickerCredentials.SetCredentials, IDsObjectPickerCredentials::SetCredentials, SetCredentials, SetCredentials method [Active Directory], SetCredentials method [Active Directory],IDsObjectPickerCredentials interface, ad.idsobjectpickercredentials_setcredentials, objsel/IDsObjectPickerCredentials::SetCredentials
req.header: objsel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
req.dll: Objsel.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDsObjectPickerCredentials::SetCredentials
 - objsel/IDsObjectPickerCredentials::SetCredentials
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Objsel.dll
api_name:
 - IDsObjectPickerCredentials.SetCredentials
---

# IDsObjectPickerCredentials::SetCredentials


## -description

Use this method to override the user credentials, passing new credentials for the account profile to be used.

## -parameters

### -param szUserName

User account.

### -param szPassword

Password.

## -returns

S_OK indicates success.

## -see-also

<a href="/windows/desktop/api/objsel/nn-objsel-idsobjectpickercredentials">IDsObjectPickerCredentials</a>