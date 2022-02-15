---
UID: NN:tsgpolicyengine.ITSGAccountingEngine
title: ITSGAccountingEngine (tsgpolicyengine.h)
description: Exposes methods that provide information about the creation or closing of sessions for a connection.
helpviewer_keywords: ["ITSGAccountingEngine","ITSGAccountingEngine interface [Remote Desktop Services]","ITSGAccountingEngine interface [Remote Desktop Services]","described","termserv.itsgaccountingengine","tsgpolicyengine/ITSGAccountingEngine"]
old-location: termserv\itsgaccountingengine.htm
tech.root: TermServ
ms.assetid: 49b402a9-137a-4cfa-89f5-12bf89c3ebb6
ms.date: 12/05/2018
ms.keywords: ITSGAccountingEngine, ITSGAccountingEngine interface [Remote Desktop Services], ITSGAccountingEngine interface [Remote Desktop Services],described, termserv.itsgaccountingengine, tsgpolicyengine/ITSGAccountingEngine
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITSGAccountingEngine
 - tsgpolicyengine/ITSGAccountingEngine
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TSGPolicyEngine.h
api_name:
 - ITSGAccountingEngine
---

# ITSGAccountingEngine interface


## -description

Exposes  methods that provide information about the creation or closing of sessions for a connection. Implement this interface when you want to receive this information from Remote Desktop Gateway (RD Gateway).

## -inheritance

The <b>ITSGAccountingEngine</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITSGAccountingEngine</b> also has these types of members:

## -remarks

Your authorization plug-in can use this interface to retrieve useful information about clients, client  computers, and remote sessions. For example, your plug-in can track the amount of time that a client is connected and the amount of data transferred during that session.

For a sample that uses the <b>ITSGAccountingEngine</b> interface, see the [Remote Desktop Gateway Pluggable Authentication and Authorization](https://github.com/microsoftarchive/msdn-code-gallery-community-m-r/tree/master/Remote%20Desktop%20Gateway%20Pluggable%20Authentication%20and%20Authorization%20Sample) sample.
