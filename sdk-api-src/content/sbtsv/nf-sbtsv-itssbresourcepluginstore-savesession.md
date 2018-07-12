---
UID: NF:sbtsv.ITsSbResourcePluginStore.SaveSession
title: ITsSbResourcePluginStore::SaveSession
author: windows-sdk-content
description: Saves a session.
old-location: termserv\itssbresourcepluginstore_savesession.htm
old-project: TermServ
ms.assetid: a4f29a99-8478-425d-91d7-c771c35bb2fa
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SaveSession method, ITsSbResourcePluginStore.SaveSession, ITsSbResourcePluginStore::SaveSession, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],SaveSession method, ITsSbResourcePluginStoreEx::SaveSession, SaveSession, SaveSession method [Remote Desktop Services], SaveSession method [Remote Desktop Services],ITsSbResourcePluginStore interface, SaveSession method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, sbtsv/ITsSbResourcePluginStore::SaveSession, sbtsv/ITsSbResourcePluginStoreEx::SaveSession, termserv.itssbresourcepluginstore_savesession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TS_SB_SORT_BY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbResourcePluginStore.SaveSession
 - ITsSbResourcePluginStoreEx.SaveSession
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITsSbResourcePluginStore::SaveSession


## -description


Saves a session.


## -parameters




### -param pSession [in]

A Pointer to the <a href="https://msdn.microsoft.com/d6f4c66a-79c3-4bc1-889d-ec5715e359ce">ITsSbSession</a> object to save.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/768a5a4e-8221-417a-ad65-9a213a176eca">ITsSbResourcePluginStoreEx</a>
 

 

