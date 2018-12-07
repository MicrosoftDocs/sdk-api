---
UID: NF:azroles.IAzApplication2.InitializeClientContext2
title: IAzApplication2::InitializeClientContext2
author: windows-sdk-content
description: Retrieves an IAzClientContext2 object pointer.
old-location: security\iazapplication2_initializeclientcontext2.htm
tech.root: secauthz
ms.assetid: 8790ebb0-97eb-47a0-b975-87e0524dcc1b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAzApplication2 interface [Security],InitializeClientContext2 method, IAzApplication2.InitializeClientContext2, IAzApplication2::InitializeClientContext2, InitializeClientContext2, InitializeClientContext2 method [Security], InitializeClientContext2 method [Security],IAzApplication2 interface, azroles/IAzApplication2::InitializeClientContext2, security.iazapplication2_initializeclientcontext2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication2.InitializeClientContext2
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplication2::InitializeClientContext2


## -description


The <b>InitializeClientContext2</b> method retrieves an <a href="https://msdn.microsoft.com/8e922370-18e3-481c-93f2-9a56d7898ba7">IAzClientContext2</a> object pointer.


## -parameters




### -param IdentifyingString [in]

A string that identifies the client context in the audit trail for client connection and object access audit entries.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppClientContext [out]

A pointer to a pointer to the returned <a href="https://msdn.microsoft.com/8e922370-18e3-481c-93f2-9a56d7898ba7">IAzClientContext2</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



