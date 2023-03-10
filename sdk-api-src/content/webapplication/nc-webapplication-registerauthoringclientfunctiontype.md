---
UID: NC:webapplication.RegisterAuthoringClientFunctionType
title: RegisterAuthoringClientFunctionType (webapplication.h)
description: Defines a pointer to an application-defined function in a dynamic-link library (DLL) that will be used as the authoring binary. When the app host starts in authoring mode, this function is called to initialize the authoring binary.
helpviewer_keywords: ["RegisterAuthoringClientFunctionType","RegisterAuthoringClientFunctionType callback","RegisterAuthoringClientFunctionType callback function [Debugging Windows Store apps]","debug.registerauthoringclientfunctiontype","webapplication/RegisterAuthoringClientFunctionType"]
old-location: debug\registerauthoringclientfunctiontype.htm
tech.root: debug
ms.assetid: 31414CBA-12A3-45F8-967B-7ECD9D90D0F6
ms.date: 12/05/2018
ms.keywords: RegisterAuthoringClientFunctionType, RegisterAuthoringClientFunctionType callback, RegisterAuthoringClientFunctionType callback function [Debugging Windows Store apps], debug.registerauthoringclientfunctiontype, webapplication/RegisterAuthoringClientFunctionType
req.header: webapplication.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - RegisterAuthoringClientFunctionType
 - webapplication/RegisterAuthoringClientFunctionType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - webapplication.h
api_name:
 - RegisterAuthoringClientFunctionType
---

# RegisterAuthoringClientFunctionType callback function


## -description

Defines a pointer to an application-defined function in a dynamic-link library (DLL) that will be used as the authoring binary. When the app host starts in authoring mode, this function is called to initialize the authoring binary.

## -parameters

### -param authoringModeObject [in]

Type: <b><a href="/previous-versions/windows/desktop/api/webapplication/nn-webapplication-iwebapplicationauthoringmode">IWebApplicationAuthoringMode</a>*</b>

An object that provides a path to the authoring binary.

### -param host [in]

Type: <b><a href="/previous-versions/windows/desktop/api/webapplication/nn-webapplication-iwebapplicationhost">IWebApplicationHost</a>*</b>

The WWAHost.

## -returns

Type: <b>HRESULT</b>

If this callback function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/webapplication/nc-webapplication-unregisterauthoringclientfunctiontype">UnregisterAuthoringClientFunctionType</a>
