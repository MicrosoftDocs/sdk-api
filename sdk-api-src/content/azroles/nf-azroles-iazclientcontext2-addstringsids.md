---
UID: NF:azroles.IAzClientContext2.AddStringSids
title: IAzClientContext2::AddStringSids
author: windows-sdk-content
description: Adds an array of string representations of security identifiers (SIDs) to the client context.
old-location: security\iazclientcontext2_addstringsids.htm
old-project: secauthz
ms.assetid: ac437686-fefb-413e-9f53-eed6c1df5798
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AddStringSids, AddStringSids method [Security], AddStringSids method [Security],IAzClientContext2 interface, IAzClientContext2 interface [Security],AddStringSids method, IAzClientContext2.AddStringSids, IAzClientContext2::AddStringSids, azroles/IAzClientContext2::AddStringSids, security.iazclientcontext2_addstringsids
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzClientContext2.AddStringSids
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzClientContext2::AddStringSids


## -description


The <b>AddStringSids</b> method adds an array of string representations of <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs) to the client context.


## -parameters




### -param varStringSids [in]

The array of string representations of SIDs to add to the client context.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



