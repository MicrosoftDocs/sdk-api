---
UID: NF:shdeprecated.IBrowserService.GetHistoryObject
title: IBrowserService::GetHistoryObject
author: windows-driver-content
description: Deprecated. Retrieves an IOleObject that represents the browser's history object.
old-location: shell\IBrowserService_GetHistoryObject.htm
old-project: shell
ms.assetid: 409d76e8-5501-437d-92d3-55e1676a80b8
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetHistoryObject, GetHistoryObject method [Windows Shell], GetHistoryObject method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],GetHistoryObject method, IBrowserService.GetHistoryObject, IBrowserService::GetHistoryObject, shdeprecated/IBrowserService::GetHistoryObject, shell.IBrowserService_GetHistoryObject, zone_IBrowserService_GetHistoryObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BNSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shdeprecated.h
api_name:
-	IBrowserService.GetHistoryObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# IBrowserService::GetHistoryObject


## -description


Deprecated. Retrieves an <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> that represents the browser's history object.


## -parameters




### -param ppole [out]

Type: <b><a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>**</b>

The address of a pointer to an <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> that represents the browser's history object.


### -param pstm [out]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>**</b>

The address of a pointer to the history object's <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>. This parameter may be <b>NULL</b>.


### -param ppbc [out]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>**</b>

The address of a pointer to the history object stream's <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>. This parameter may be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <i>pstm</i> is not <b>NULL</b>, you can call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> to get a pointer to <a href="_inet_IPersistHistory_Interface">IPersistHistory</a>.


<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> and <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> can be passed to <a href="_inet_IPersistHistory_Interface_inet_IPersistHistory_LoadHistory_Method_cpp">IPersistHistory::LoadHistory</a>.

The calling application must release all three pointers if non-<b>NULL</b>.



