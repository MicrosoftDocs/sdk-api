---
UID: NF:shdeprecated.IBrowserService.GetNavigateState
title: IBrowserService::GetNavigateState
author: windows-sdk-content
description: Deprecated. Retrieves the browser's current navigation state.
old-location: shell\IBrowserService_GetNavigateState.htm
old-project: shell
ms.assetid: 5a8aac75-3e0b-4ff2-a1ec-e08379e67c84
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: BNS_BEGIN_NAVIGATE, BNS_NAVIGATE, BNS_NORMAL, GetNavigateState, GetNavigateState method [Windows Shell], GetNavigateState method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],GetNavigateState method, IBrowserService.GetNavigateState, IBrowserService::GetNavigateState, shdeprecated/IBrowserService::GetNavigateState, shell.IBrowserService_GetNavigateState, zone_IBrowserService_GetNavigateState
ms.prod: windows
ms.technology: windows-sdk
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
 - IBrowserService.GetNavigateState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# IBrowserService::GetNavigateState


## -description


Deprecated. Retrieves the browser's current navigation state.


## -parameters




### -param pbnstate [out]

Type: <b><a href="https://msdn.microsoft.com/e49f38f0-51d3-43a7-96f6-1722a4afa848">BNSTATE</a>*</b>

A pointer to a value from the <a href="https://msdn.microsoft.com/e49f38f0-51d3-43a7-96f6-1722a4afa848">BNSTATE</a> enumeration indicating the current navigation state.



#### BNS_NORMAL (0)

The normal state.



#### BNS_BEGIN_NAVIGATE (1)

A begin navigation event has occurred.



#### BNS_NAVIGATE (2)

A navigation event has occurred.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



