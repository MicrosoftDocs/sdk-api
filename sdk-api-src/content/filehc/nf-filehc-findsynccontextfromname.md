---
UID: NF:filehc.FindSyncContextFromName
title: FindSyncContextFromName function
author: windows-sdk-content
description: Retrieves the FIO_CONTEXT structure that is associated with the specified user name.
old-location: winprog\_findsynccontextfromname.htm
tech.root: devnotes
ms.assetid: 1528b545-6d04-4315-a0ca-cebef6144fe9
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: FindSyncContextFromName, FindSyncContextFromName function [Windows API], filehc/FindSyncContextFromName, winprog._findsynccontextfromname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: filehc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Fcachdll.lib
req.dll: Fcachdll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fcachdll.dll
api_name:
 - FindSyncContextFromName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FindSyncContextFromName function


## -description


Retrieves the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure that is associated with the specified user name.


## -parameters




### -param pNameCache [in]

A pointer to the name cache that the client is to use.


### -param lpbName [in]

A pointer to the name of the cached item.


### -param cbName [in]

The size, in bytes, of the value in <i>lpbName</i>.


### -param pfnCallback [in]

A pointer to a <a href="https://msdn.microsoft.com/9fcdbca6-95db-4ec1-b81c-3681e9e2bffb">FCACHE_READ_CALLBACK</a> function.

<div class="alert"><b>Note</b>  If this parameter is <b>NULL</b>, no callback function is called.</div>
<div> </div>

### -param lpvClientContext [in]

A pointer to the context that is associated with the client. This context is passed to the callback function.


### -param hToken [in]

Request the cache to evaluate the embedded security descriptor. If <i>hToken</i> is zero, it is ignored.


### -param accessMask [in]

The security descriptor data. For more information, see <a href="https://msdn.microsoft.com/f115ee54-3333-4109-8004-d71904a7a943">ACCESS_MASK</a>.


### -param ppContext [out]

A pointer to a pointer to the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure that is associated with the user name.

If the function returns <b>TRUE</b>, this parameter can return a <b>NULL</b> pointer. This occurs when the user passes a <b>NULL</b> FIO_CONTEXT to <a href="https://msdn.microsoft.com/4f4bbfda-3be0-41d3-9087-d46edd2e21a3">_AssociateContextWithName</a>.


## -returns



Returns <b>TRUE</b> if the name is found in the cache; otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/f115ee54-3333-4109-8004-d71904a7a943">ACCESS_MASK</a>



<a href="https://msdn.microsoft.com/4f4bbfda-3be0-41d3-9087-d46edd2e21a3">AssociateContextWithName</a>



<a href="https://msdn.microsoft.com/9fcdbca6-95db-4ec1-b81c-3681e9e2bffb">FCACHE_READ_CALLBACK</a>



<a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a>
 

 

