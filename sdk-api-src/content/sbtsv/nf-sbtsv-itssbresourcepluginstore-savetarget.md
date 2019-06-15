---
UID: NF:sbtsv.ITsSbResourcePluginStore.SaveTarget
title: ITsSbResourcePluginStore::SaveTarget (sbtsv.h)
author: windows-sdk-content
description: Saves a target.
old-location: termserv\itssbresourcepluginstore_savetarget.htm
tech.root: TermServ
ms.assetid: 323ac6ee-6a50-433b-85b3-a4409be08226
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SaveTarget method, ITsSbResourcePluginStore.SaveTarget, ITsSbResourcePluginStore::SaveTarget, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],SaveTarget method, ITsSbResourcePluginStoreEx::SaveTarget, SaveTarget, SaveTarget method [Remote Desktop Services], SaveTarget method [Remote Desktop Services],ITsSbResourcePluginStore interface, SaveTarget method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, sbtsv/ITsSbResourcePluginStore::SaveTarget, sbtsv/ITsSbResourcePluginStoreEx::SaveTarget, termserv.itssbresourcepluginstore_savetarget
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
 - ITsSbResourcePluginStore.SaveTarget
 - ITsSbResourcePluginStoreEx.SaveTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbResourcePluginStore::SaveTarget


## -description


Saves a target.


## -parameters




### -param pTarget [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a> object to save.


### -param bForceWrite [in]

Set to TRUE to force writing the saved object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="https://docs.microsoft.com/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a>
 

 

