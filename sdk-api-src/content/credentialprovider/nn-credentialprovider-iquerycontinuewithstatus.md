---
UID: NN:credentialprovider.IQueryContinueWithStatus
title: IQueryContinueWithStatus (credentialprovider.h)
description: Exposes methods that provide a standard mechanism for credential providers to call QueryContinue while attempting to connect to the network to determine if they should continue these attempts.
helpviewer_keywords: ["IQueryContinueWithStatus","IQueryContinueWithStatus interface [Windows Shell]","IQueryContinueWithStatus interface [Windows Shell]","described","_shell_IQueryContinueWithStatus","credentialprovider/IQueryContinueWithStatus","shell.IQueryContinueWithStatus"]
old-location: shell\IQueryContinueWithStatus.htm
tech.root: shell
ms.assetid: 3f41714e-d8f6-46ea-aea4-19dca4723ca5
ms.date: 12/05/2018
ms.keywords: IQueryContinueWithStatus, IQueryContinueWithStatus interface [Windows Shell], IQueryContinueWithStatus interface [Windows Shell],described, _shell_IQueryContinueWithStatus, credentialprovider/IQueryContinueWithStatus, shell.IQueryContinueWithStatus
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Credentialprovider.idl
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
 - IQueryContinueWithStatus
 - credentialprovider/IQueryContinueWithStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Credentialprovider.h
api_name:
 - IQueryContinueWithStatus
---

# IQueryContinueWithStatus interface


## -description

Exposes methods that provide a standard mechanism for credential providers to call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iquerycontinue-querycontinue">QueryContinue</a> while attempting to connect to the network to determine if they should continue these attempts. Credential providers can also use this interface to display messages to the user while attempting to establish a network connection.

## -inheritance

The <b>IQueryContinueWithStatus</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue">IQueryContinue</a>. <b>IQueryContinueWithStatus</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue">IQueryContinue</a> interface, from which it inherits.
