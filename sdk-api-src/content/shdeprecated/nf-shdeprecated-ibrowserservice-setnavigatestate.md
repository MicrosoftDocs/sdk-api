---
UID: NF:shdeprecated.IBrowserService.SetNavigateState
title: IBrowserService::SetNavigateState (shdeprecated.h)
description: Deprecated. Sets the current navigation state. This method affects the cursor and animation.
helpviewer_keywords: ["BNS_BEGIN_NAVIGATE","BNS_NAVIGATE","BNS_NORMAL","IBrowserService interface [Windows Shell]","SetNavigateState method","IBrowserService.SetNavigateState","IBrowserService::SetNavigateState","SetNavigateState","SetNavigateState method [Windows Shell]","SetNavigateState method [Windows Shell]","IBrowserService interface","shdeprecated/IBrowserService::SetNavigateState","shell.IBrowserService_SetNavigateState","zone_IBrowserService_SetNavigateState"]
old-location: shell\IBrowserService_SetNavigateState.htm
tech.root: shell
ms.assetid: 3cdbe902-f208-43f8-9019-d61c22635196
ms.date: 12/05/2018
ms.keywords: BNS_BEGIN_NAVIGATE, BNS_NAVIGATE, BNS_NORMAL, IBrowserService interface [Windows Shell],SetNavigateState method, IBrowserService.SetNavigateState, IBrowserService::SetNavigateState, SetNavigateState, SetNavigateState method [Windows Shell], SetNavigateState method [Windows Shell],IBrowserService interface, shdeprecated/IBrowserService::SetNavigateState, shell.IBrowserService_SetNavigateState, zone_IBrowserService_SetNavigateState
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
 - IBrowserService::SetNavigateState
 - shdeprecated/IBrowserService::SetNavigateState
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
 - IBrowserService.SetNavigateState
---

# IBrowserService::SetNavigateState


## -description

Deprecated. Sets the current navigation state. This method affects the cursor and animation.

## -parameters

### -param bnstate [in]

Type: <b><a href="/windows/desktop/api/shdeprecated/ne-shdeprecated-bnstate">BNSTATE</a></b>

The value from the <a href="/windows/desktop/api/shdeprecated/ne-shdeprecated-bnstate">BNSTATE</a> enumeration that indicates the navigation state.



#### BNS_NORMAL (0)

The normal state.



#### BNS_BEGIN_NAVIGATE (1)

A begin navigation event has occurred.



#### BNS_NAVIGATE (2)

A navigation event has occurred.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.