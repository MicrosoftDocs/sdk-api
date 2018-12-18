---
UID: NF:wdstpdi.WdsTransportProviderUserAccessCheck
title: WdsTransportProviderUserAccessCheck function
author: windows-sdk-content
description: Specifies access to a content stream based on a user's token.
old-location: wds\wdstransportprovideruseraccesscheck.htm
tech.root: wds
ms.assetid: 3ce381d3-d6f6-4f64-a825-116c3cff4747
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WdsTransportProviderUserAccessCheck, WdsTransportProviderUserAccessCheck callback, WdsTransportProviderUserAccessCheck callback function [Windows Deployment Services], wds.wdstransportprovideruseraccesscheck, wdstpdi/WdsTransportProviderUserAccessCheck
ms.topic: function
req.header: wdstpdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - UserDefined
api_location:
 - wdstpdi.h
api_name:
 - WdsTransportProviderUserAccessCheck
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WdsTransportProviderUserAccessCheck function


## -description


Specifies access to a content stream based on a user's token. 


## -parameters




### -param hContent [in]

Handle to an open content stream to be read. This is the handle return by the <a href="https://msdn.microsoft.com/95bea971-9c97-4d66-871d-5ef7407b9659">WdsTransportProviderOpenContent</a> callback.


### -param hUserToken [in]

The token of the user whose access should be checked.


### -param pbAccessAllowed [out]

Pointer to a boolean value. The content provider should set this value to <b>TRUE</b> if it allows the user access to the content stream.  The content provider should set this value to <b>FALSE</b> if it does not allow the user access to the content stream.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



This callback is required.



