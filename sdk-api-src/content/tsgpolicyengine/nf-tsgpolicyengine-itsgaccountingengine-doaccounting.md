---
UID: NF:tsgpolicyengine.ITSGAccountingEngine.DoAccounting
title: ITSGAccountingEngine::DoAccounting
author: windows-sdk-content
description: Provides information about the creation or closing of sessions for a connection.
old-location: termserv\itsgaccountingengine_doaccounting.htm
tech.root: TermServ
ms.assetid: ebc57caa-804b-46a4-96bb-8b50c13029ab
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DoAccounting, DoAccounting method [Remote Desktop Services], DoAccounting method [Remote Desktop Services],ITSGAccountingEngine interface, ITSGAccountingEngine interface [Remote Desktop Services],DoAccounting method, ITSGAccountingEngine.DoAccounting, ITSGAccountingEngine::DoAccounting, termserv.itsgaccountingengine_doaccounting, tsgpolicyengine/ITSGAccountingEngine::DoAccounting
ms.topic: method
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
---

# ITSGAccountingEngine::DoAccounting


## -description


Provides information about the creation or closing of sessions for a connection.

Remote Desktop Gateway (RD Gateway) calls this method to pass information to an authorization plug-in.


## -parameters




### -param accountingDataType [in]

A value of the <a href="https://msdn.microsoft.com/2864d044-266c-44e4-90d3-ccd75bf08348">AAAccountingDataType</a> 
      enumeration type that specifies the type of event that occurred.


### -param accountingData [in]

An <a href="https://msdn.microsoft.com/1c79f910-8dd9-47dc-80d1-f6252f0a43dd">AAAccountingData</a> structure that contains 
       information about the event that occurred.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/49b402a9-137a-4cfa-89f5-12bf89c3ebb6">ITSGAccountingEngine</a>
 

 

