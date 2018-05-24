---
UID: NF:recapis.GetRightSeparator
title: GetRightSeparator function
author: windows-driver-content
description: Gets the right separator for the recognizer context.
old-location: tablet\getrightseparator.htm
old-project: tablet
ms.assetid: 1fc11447-3125-4853-bba6-2784e69d033e
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: GetRightSeparator, GetRightSeparator function [Tablet PC], recapis/GetRightSeparator, tablet.getrightseparator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	recapis.h
api_name:
-	GetRightSeparator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# GetRightSeparator function


## -description


Gets the right separator for the recognizer context.


## -parameters




### -param hrc

The handle to the recognizer context.


### -param pcSize [in, out]

A pointer to the size of the right separator.


### -param pwcRightSeparator [out, optional]

A pointer to the right separator.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



