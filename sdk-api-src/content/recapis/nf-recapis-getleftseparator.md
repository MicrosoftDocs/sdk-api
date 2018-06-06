---
UID: NF:recapis.GetLeftSeparator
title: GetLeftSeparator function
author: windows-sdk-content
description: Gets the left separator for the recognizer context.
old-location: tablet\getleftseparator.htm
old-project: tablet
ms.assetid: 5528d31e-580f-4da7-b683-e9ea2931989b
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: GetLeftSeparator, GetLeftSeparator function [Tablet PC], recapis/GetLeftSeparator, tablet.getleftseparator
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - GetLeftSeparator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# GetLeftSeparator function


## -description


Gets the left separator for the recognizer context.


## -parameters




### -param hrc

The handle to the recognizer context.


### -param pcSize [in, out]

A pointer to the size of the left separator.


### -param pwcLeftSeparator [out]

A pointer to the left separator.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



