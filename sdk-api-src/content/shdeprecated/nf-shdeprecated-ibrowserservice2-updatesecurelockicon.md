---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IBrowserService2::UpdateSecureLockIcon


## -description


Deprecated. Updates the value of the <b>_eSecureLockIcon</b> member of the <a href="https://msdn.microsoft.com/d56e42e8-a556-4470-82d9-466edd84214f">BASEBROWSERDATA</a> structure, which tracks the icon indicating a secure site, as well as updating the icon itself in the UI.


## -parameters




### -param eSecureLock [in]

Type: <b>int</b>

One of the following values indicating the secure lock status. Note that each value is provided in a SET and SUGGEST form. For more details, see <a href="https://msdn.microsoft.com/d56e42e8-a556-4470-82d9-466edd84214f">BASEBROWSERDATA</a>.





#### SECURELOCK_NOCHANGE



#### SECURELOCK_SET_UNSECURE



#### SECURELOCK_SET_MIXED



#### SECURELOCK_SET_SECUREUNKNOWNBIT



#### SECURELOCK_SET_SECURE40BIT



#### SECURELOCK_SET_SECURE56BIT



#### SECURELOCK_SET_FORTEZZA



#### SECURELOCK_SET_SECURE128BIT



#### SECURELOCK_FIRSTSUGGEST



#### SECURELOCK_SUGGEST_UNSECURE



#### SECURELOCK_SUGGEST_MIXED



#### SECURELOCK_SUGGEST_SECUREUNKNOWNBIT



#### SECURELOCK_SUGGEST_SECURE40BIT



#### SECURELOCK_SUGGEST_SECURE56BIT



#### SECURELOCK_SUGGEST_FORTEZZA



#### SECURELOCK_SUGGEST_SECURE128BIT


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



SECURELOCK_SUGGEST_UNSECURE is equivalent to SECURELOCK_FIRSTSUGGEST.



