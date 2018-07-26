---
UID: NF:shobjidl_core.IQueryContinue.QueryContinue
title: IQueryContinue::QueryContinue
author: windows-sdk-content
description: Returns S_OK if the operation associated with the current instance of this interface should continue.
old-location: shell\IQueryContinue_QueryContinue.htm
old-project: shell
ms.assetid: 9beabfc9-56b9-4778-8027-939aa986086a
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IQueryContinue interface [Windows Shell],QueryContinue method, IQueryContinue.QueryContinue, IQueryContinue::QueryContinue, QueryContinue, QueryContinue method [Windows Shell], QueryContinue method [Windows Shell],IQueryContinue interface, inet_IQueryContinue_QueryContinue, shell.IQueryContinue_QueryContinue, shobjidl_core/IQueryContinue::QueryContinue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IQueryContinue.QueryContinue
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IQueryContinue::QueryContinue


## -description


Returns <b>S_OK</b> if the operation associated with the current instance of this interface should continue.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the calling application should continue, <b>S_FALSE</b> if not.




## -remarks



In typical usage, a pointer to an <a href="https://msdn.microsoft.com/94dee6cc-a142-4180-a562-14f4ded16884">IQueryContinue</a> interface is passed to a method of another object.	That object, in turn, runs this method periodically to determine whether to continue its actions. For example, if a user clicks a cancel button, this method will start returning <b>S_FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/94dee6cc-a142-4180-a562-14f4ded16884">IQueryContinue</a>



<a href="https://msdn.microsoft.com/24ff171c-e9e2-4d62-8a8c-d62e5d7a92ad">IUserNotification</a>
 

 

