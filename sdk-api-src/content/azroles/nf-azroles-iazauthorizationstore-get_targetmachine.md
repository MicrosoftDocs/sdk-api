---
UID: NF:azroles.IAzAuthorizationStore.get_TargetMachine
title: IAzAuthorizationStore::get_TargetMachine (azroles.h)
description: Retrieves the name of the computer on which account resolution should occur.
helpviewer_keywords: ["AzAuthorizationStore object [Security]","TargetMachine property","IAzAuthorizationStore interface [Security]","TargetMachine property","IAzAuthorizationStore.TargetMachine","IAzAuthorizationStore.get_TargetMachine","IAzAuthorizationStore::TargetMachine","IAzAuthorizationStore::get_TargetMachine","TargetMachine property [Security]","TargetMachine property [Security]","AzAuthorizationStore object","TargetMachine property [Security]","IAzAuthorizationStore interface","azroles/IAzAuthorizationStore::TargetMachine","azroles/IAzAuthorizationStore::get_TargetMachine","get_TargetMachine","security.azauthorizationstore_targetmachine"]
old-location: security\azauthorizationstore_targetmachine.htm
tech.root: security
ms.assetid: 60c3c23a-4721-4f0d-8380-e95b6170c804
ms.date: 12/05/2018
ms.keywords: AzAuthorizationStore object [Security],TargetMachine property, IAzAuthorizationStore interface [Security],TargetMachine property, IAzAuthorizationStore.TargetMachine, IAzAuthorizationStore.get_TargetMachine, IAzAuthorizationStore::TargetMachine, IAzAuthorizationStore::get_TargetMachine, TargetMachine property [Security], TargetMachine property [Security],AzAuthorizationStore object, TargetMachine property [Security],IAzAuthorizationStore interface, azroles/IAzAuthorizationStore::TargetMachine, azroles/IAzAuthorizationStore::get_TargetMachine, get_TargetMachine, security.azauthorizationstore_targetmachine
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzAuthorizationStore::get_TargetMachine
 - azroles/IAzAuthorizationStore::get_TargetMachine
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzAuthorizationStore.TargetMachine
 - IAzAuthorizationStore.get_TargetMachine
 - AzAuthorizationStore.TargetMachine
---

# IAzAuthorizationStore::get_TargetMachine


## -description

The <b>TargetMachine</b> property retrieves the name of the computer on which account resolution should occur.

This property is read-only.

## -parameters

## -remarks

Determination of the target computer takes into consideration active directories in local and remote domains, Distributed File System (DFS) shares, mount point, local drive, remote mapped shares, and so on.

