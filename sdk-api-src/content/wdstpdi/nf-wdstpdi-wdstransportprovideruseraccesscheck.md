---
UID: NF:wdstpdi.WdsTransportProviderUserAccessCheck
title: WdsTransportProviderUserAccessCheck function (wdstpdi.h)
description: Specifies access to a content stream based on a user's token.
helpviewer_keywords: ["WdsTransportProviderUserAccessCheck","WdsTransportProviderUserAccessCheck callback","WdsTransportProviderUserAccessCheck callback function [Windows Deployment Services]","wds.wdstransportprovideruseraccesscheck","wdstpdi/WdsTransportProviderUserAccessCheck"]
old-location: wds\wdstransportprovideruseraccesscheck.htm
tech.root: wds
ms.assetid: 3ce381d3-d6f6-4f64-a825-116c3cff4747
ms.date: 12/05/2018
ms.keywords: WdsTransportProviderUserAccessCheck, WdsTransportProviderUserAccessCheck callback, WdsTransportProviderUserAccessCheck callback function [Windows Deployment Services], wds.wdstransportprovideruseraccesscheck, wdstpdi/WdsTransportProviderUserAccessCheck
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsTransportProviderUserAccessCheck
 - wdstpdi/WdsTransportProviderUserAccessCheck
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - wdstpdi.h
api_name:
 - WdsTransportProviderUserAccessCheck
---

# WdsTransportProviderUserAccessCheck function


## -description

Specifies access to a content stream based on a user's token.

## -parameters

### -param hContent [in]

Handle to an open content stream to be read. This is the handle return by the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent">WdsTransportProviderOpenContent</a> callback.

### -param hUserToken [in]

The token of the user whose access should be checked.

### -param pbAccessAllowed [out]

Pointer to a boolean value. The content provider should set this value to <b>TRUE</b> if it allows the user access to the content stream.  The content provider should set this value to <b>FALSE</b> if it does not allow the user access to the content stream.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

This callback is required.