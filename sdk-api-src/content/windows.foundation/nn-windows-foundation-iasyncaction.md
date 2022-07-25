---
UID: NN:windows.foundation.IAsyncAction
title: IAsyncAction (windows.foundation.h)
description: Represents an asynchronous action.
helpviewer_keywords: ["IAsyncAction","IAsyncAction interface [Windows Runtime]","IAsyncAction interface [Windows Runtime]","described","windows/IAsyncAction","winrt.iasyncaction"]
old-location: winrt\iasyncaction.htm
tech.root: WinRT
ms.assetid: E5D567F6-FFDE-4E51-8D52-638D30252549
ms.date: 12/05/2018
ms.keywords: IAsyncAction, IAsyncAction interface [Windows Runtime], IAsyncAction interface [Windows Runtime],described, windows/IAsyncAction, winrt.iasyncaction
req.header: windows.foundation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Foundation.idl
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
ms.custom: 19H1
f1_keywords:
 - IAsyncAction
 - windows.foundation/IAsyncAction
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.Foundation.h
api_name:
 - IAsyncAction
---

# IAsyncAction interface


## -description

Represents an asynchronous action.

## -inheritance

The <b>IAsyncAction</b> interface inherits from <b>IInspectable</b>. <b>IAsyncAction</b> also has these types of members:

## -remarks

The <b>IAsyncAction</b> interface represents an asynchronous action that does not return a result and does not have progress notifications.  When the action completes, the <a href="/windows/desktop/WinRT/asyncactioncompletedhandler">AsyncActionCompletedHandler</a> specified by <a href="/windows/desktop/WinRT/iasyncaction-get-completed">get_Completed</a>  is invoked, and this is the only result from the action.
