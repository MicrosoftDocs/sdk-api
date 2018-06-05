---
UID: NF:shdeprecated.IBrowserService.SetNavigateState
title: IBrowserService::SetNavigateState
author: windows-sdk-content
description: Deprecated. Sets the current navigation state. This method affects the cursor and animation.
old-location: shell\IBrowserService_SetNavigateState.htm
old-project: shell
ms.assetid: 3cdbe902-f208-43f8-9019-d61c22635196
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: BNS_BEGIN_NAVIGATE, BNS_NAVIGATE, BNS_NORMAL, IBrowserService interface [Windows Shell],SetNavigateState method, IBrowserService.SetNavigateState, IBrowserService::SetNavigateState, SetNavigateState, SetNavigateState method [Windows Shell], SetNavigateState method [Windows Shell],IBrowserService interface, shdeprecated/IBrowserService::SetNavigateState, shell.IBrowserService_SetNavigateState, zone_IBrowserService_SetNavigateState
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shdeprecated.h
api_name:
-	IBrowserService.SetNavigateState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# IBrowserService::SetNavigateState


## -description


Deprecated. Sets the current navigation state. This method affects the cursor and animation.


## -parameters




### -param bnstate [in]

Type: <b><a href="https://msdn.microsoft.com/e49f38f0-51d3-43a7-96f6-1722a4afa848">BNSTATE</a></b>

The value from the <a href="https://msdn.microsoft.com/e49f38f0-51d3-43a7-96f6-1722a4afa848">BNSTATE</a> enumeration that indicates the navigation state.



#### BNS_NORMAL (0)

The normal state.



#### BNS_BEGIN_NAVIGATE (1)

A begin navigation event has occurred.



#### BNS_NAVIGATE (2)

A navigation event has occurred.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



