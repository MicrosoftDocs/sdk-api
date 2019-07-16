---
UID: NF:tsgpolicyengine.ITSGAccountingEngine.DoAccounting
title: ITSGAccountingEngine::DoAccounting (tsgpolicyengine.h)
author: windows-sdk-content
description: Provides information about the creation or closing of sessions for a connection.
old-location: termserv\itsgaccountingengine_doaccounting.htm
tech.root: TermServ
ms.assetid: ebc57caa-804b-46a4-96bb-8b50c13029ab
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DoAccounting, DoAccounting method [Remote Desktop Services], DoAccounting method [Remote Desktop Services],ITSGAccountingEngine interface, ITSGAccountingEngine interface [Remote Desktop Services],DoAccounting method, ITSGAccountingEngine.DoAccounting, ITSGAccountingEngine::DoAccounting, termserv.itsgaccountingengine_doaccounting, tsgpolicyengine/ITSGAccountingEngine::DoAccounting
ms.topic: method
f1_keywords: 
 - "tsgpolicyengine/ITSGAccountingEngine.DoAccounting"
req.header: tsgpolicyengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSGPolicyEngine.idl
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
 - TSGPolicyEngine.h
api_name:
 - ITSGAccountingEngine.DoAccounting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITSGAccountingEngine::DoAccounting


## -description


Provides information about the creation or closing of sessions for a connection.

Remote Desktop Gateway (RD Gateway) calls this method to pass information to an authorization plug-in.


## -parameters




### -param accountingDataType [in]

A value of the <a href="https://docs.microsoft.com/windows/win32/api/tsgpolicyengine/ns-tsgpolicyengine-aaaccountingdata">AAAccountingDataType</a> 
      enumeration type that specifies the type of event that occurred.


### -param accountingData [in]

An <a href="https://docs.microsoft.com/windows/win32/api/tsgpolicyengine/ns-tsgpolicyengine-aaaccountingdata">AAAccountingData</a> structure that contains 
       information about the event that occurred.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tsgpolicyengine/nn-tsgpolicyengine-itsgaccountingengine">ITSGAccountingEngine</a>
 

 

