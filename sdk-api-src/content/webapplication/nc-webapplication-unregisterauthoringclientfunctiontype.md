---
UID: NC:webapplication.UnregisterAuthoringClientFunctionType
title: UnregisterAuthoringClientFunctionType (webapplication.h)
description: Unregisters the application-defined function that was registered with the RegisterAuthoringClientFunctionType function. This function is called when the app host terminates.
helpviewer_keywords: ["UnregisterAuthoringClientFunctionType","UnregisterAuthoringClientFunctionType callback","UnregisterAuthoringClientFunctionType callback function [Debugging Windows Store apps]","debug.unregisterauthoringclientfunctiontype","webapplication/UnregisterAuthoringClientFunctionType"]
old-location: debug\unregisterauthoringclientfunctiontype.htm
tech.root: debug
ms.assetid: 2F48142B-88D2-49B7-9FAA-5D6BA4DC3837
ms.date: 12/05/2018
ms.keywords: UnregisterAuthoringClientFunctionType, UnregisterAuthoringClientFunctionType callback, UnregisterAuthoringClientFunctionType callback function [Debugging Windows Store apps], debug.unregisterauthoringclientfunctiontype, webapplication/UnregisterAuthoringClientFunctionType
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
 - UnregisterAuthoringClientFunctionType
 - webapplication/UnregisterAuthoringClientFunctionType
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
 - UnregisterAuthoringClientFunctionType
---

# UnregisterAuthoringClientFunctionType callback function


## -description

Unregisters the application-defined function that was registered with the <a href="/previous-versions/windows/desktop/api/webapplication/nc-webapplication-registerauthoringclientfunctiontype">RegisterAuthoringClientFunctionType</a> function. This function is called when the app host  terminates.

## -parameters

### -param host [in]

Type: <b><a href="/previous-versions/windows/desktop/api/webapplication/nn-webapplication-iwebapplicationhost">IWebApplicationHost</a>*</b>

An object that provides a path to the authoring binary.

## -returns

Type: <b>HRESULT</b>

The WWAHost.

## -see-also

<a href="/previous-versions/windows/desktop/api/webapplication/nc-webapplication-registerauthoringclientfunctiontype">RegisterAuthoringClientFunctionType</a>
