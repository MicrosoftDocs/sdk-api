---
UID: NF:shdeprecated.IBrowserService.SetHistoryObject
title: IBrowserService::SetHistoryObject
author: windows-sdk-content
description: Deprecated. Sets the browser's history object.
old-location: shell\IBrowserService_SetHistoryObject.htm
old-project: shell
ms.assetid: 1a0b55b0-a6b6-4b0c-be09-cfb573a5420c
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IBrowserService interface [Windows Shell],SetHistoryObject method, IBrowserService.SetHistoryObject, IBrowserService::SetHistoryObject, SetHistoryObject, SetHistoryObject method [Windows Shell], SetHistoryObject method [Windows Shell],IBrowserService interface, shdeprecated/IBrowserService::SetHistoryObject, shell.IBrowserService_SetHistoryObject, zone_IBrowserService_SetHistoryObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: BNSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService.SetHistoryObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# IBrowserService::SetHistoryObject


## -description


Deprecated. Sets the browser's history object.


## -parameters




### -param pole [in]

Type: <b><a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> that represents the history object to set.


### -param fIsLocalAnchor [in]

Type: <b>BOOL</b>

A value that specifies whether the new entry is a local or a remote file. Used in the case of the reuse of an inner object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method will fail if the browser already has a history object.



