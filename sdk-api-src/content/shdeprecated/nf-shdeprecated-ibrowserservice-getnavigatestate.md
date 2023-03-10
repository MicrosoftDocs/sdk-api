---
UID: NF:shdeprecated.IBrowserService.GetNavigateState
title: IBrowserService::GetNavigateState (shdeprecated.h)
description: Deprecated. Retrieves the browser's current navigation state.
helpviewer_keywords: ["BNS_BEGIN_NAVIGATE","BNS_NAVIGATE","BNS_NORMAL","GetNavigateState","GetNavigateState method [Windows Shell]","GetNavigateState method [Windows Shell]","IBrowserService interface","IBrowserService interface [Windows Shell]","GetNavigateState method","IBrowserService.GetNavigateState","IBrowserService::GetNavigateState","shdeprecated/IBrowserService::GetNavigateState","shell.IBrowserService_GetNavigateState","zone_IBrowserService_GetNavigateState"]
old-location: shell\IBrowserService_GetNavigateState.htm
tech.root: shell
ms.assetid: 5a8aac75-3e0b-4ff2-a1ec-e08379e67c84
ms.date: 12/05/2018
ms.keywords: BNS_BEGIN_NAVIGATE, BNS_NAVIGATE, BNS_NORMAL, GetNavigateState, GetNavigateState method [Windows Shell], GetNavigateState method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],GetNavigateState method, IBrowserService.GetNavigateState, IBrowserService::GetNavigateState, shdeprecated/IBrowserService::GetNavigateState, shell.IBrowserService_GetNavigateState, zone_IBrowserService_GetNavigateState
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService::GetNavigateState
 - shdeprecated/IBrowserService::GetNavigateState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService.GetNavigateState
---

# IBrowserService::GetNavigateState


## -description

Deprecated. Retrieves the browser's current navigation state.

## -parameters

### -param pbnstate [out]

Type: <b><a href="/windows/desktop/api/shdeprecated/ne-shdeprecated-bnstate">BNSTATE</a>*</b>

A pointer to a value from the <a href="/windows/desktop/api/shdeprecated/ne-shdeprecated-bnstate">BNSTATE</a> enumeration indicating the current navigation state.



#### BNS_NORMAL (0)

The normal state.



#### BNS_BEGIN_NAVIGATE (1)

A begin navigation event has occurred.



#### BNS_NAVIGATE (2)

A navigation event has occurred.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.