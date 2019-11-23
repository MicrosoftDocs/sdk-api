---
UID: NF:sbtsv.ITsSbResourcePluginStore.QuerySessionBySessionId
title: ITsSbResourcePluginStore::QuerySessionBySessionId (sbtsv.h)

description: Returns the session object that has the specified session ID.
old-location: termserv\itssbresourcepluginstore_querysessionbysessionid.htm
tech.root: TermServ
ms.assetid: 51a1e876-09fb-4b1c-bb86-028afc46f31e

ms.date: 12/05/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],QuerySessionBySessionId method, ITsSbResourcePluginStore.QuerySessionBySessionId, ITsSbResourcePluginStore::QuerySessionBySessionId, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],QuerySessionBySessionId method, ITsSbResourcePluginStoreEx::QuerySessionBySessionId, QuerySessionBySessionId, QuerySessionBySessionId method [Remote Desktop Services], QuerySessionBySessionId method [Remote Desktop Services],ITsSbResourcePluginStore interface, QuerySessionBySessionId method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, sbtsv/ITsSbResourcePluginStore::QuerySessionBySessionId, sbtsv/ITsSbResourcePluginStoreEx::QuerySessionBySessionId, termserv.itssbresourcepluginstore_querysessionbysessionid
ms.topic: method
f1_keywords: 
 - "sbtsv/ITsSbResourcePluginStore.QuerySessionBySessionId"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbResourcePluginStore.QuerySessionBySessionId
 - ITsSbResourcePluginStoreEx.QuerySessionBySessionId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbResourcePluginStore::QuerySessionBySessionId


## -description


Returns the session object that has the specified session ID.


## -parameters




### -param dwSessionId [in]

The session ID.


### -param TargetName [in]

The target name.


### -param ppSession [out]

A pointer to a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession">ITsSbSession</a> session object. When you have finished using the object, release it by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A resource plug-in can use this method to retrieve a session object. Unlike the global store, the resource plug-in store does not copy the session object retrieved because the resource plug-in owns the session object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="https://docs.microsoft.com/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession">ITsSbSession</a>
 

 

