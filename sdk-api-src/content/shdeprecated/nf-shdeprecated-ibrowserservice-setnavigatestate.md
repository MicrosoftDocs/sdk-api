---
UID: NF:shdeprecated.IBrowserService.SetNavigateState
title: IBrowserService::SetNavigateState (shdeprecated.h)
author: windows-sdk-content
description: Deprecated. Sets the current navigation state. This method affects the cursor and animation.
old-location: shell\IBrowserService_SetNavigateState.htm
tech.root: shell
ms.assetid: 3cdbe902-f208-43f8-9019-d61c22635196
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BNS_BEGIN_NAVIGATE, BNS_NAVIGATE, BNS_NORMAL, IBrowserService interface [Windows Shell],SetNavigateState method, IBrowserService.SetNavigateState, IBrowserService::SetNavigateState, SetNavigateState, SetNavigateState method [Windows Shell], SetNavigateState method [Windows Shell],IBrowserService interface, shdeprecated/IBrowserService::SetNavigateState, shell.IBrowserService_SetNavigateState, zone_IBrowserService_SetNavigateState
ms.topic: method
f1_keywords: ["shdeprecated/IBrowserService.SetNavigateState"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService.SetNavigateState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
---

# IBrowserService::SetNavigateState


## -description


Deprecated. Sets the current navigation state. This method affects the cursor and animation.


## -parameters




### -param bnstate [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/ne-shdeprecated-tagbnstate">BNSTATE</a></b>

The value from the <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/ne-shdeprecated-tagbnstate">BNSTATE</a> enumeration that indicates the navigation state.



#### BNS_NORMAL (0)

The normal state.



#### BNS_BEGIN_NAVIGATE (1)

A begin navigation event has occurred.



#### BNS_NAVIGATE (2)

A navigation event has occurred.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



