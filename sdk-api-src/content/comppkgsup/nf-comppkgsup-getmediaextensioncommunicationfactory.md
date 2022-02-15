---
UID: NF:comppkgsup.GetMediaExtensionCommunicationFactory
title: GetMediaExtensionCommunicationFactory function (comppkgsup.h)
description: Creates a communication factory for registering a media extension.
helpviewer_keywords: ["GetMediaExtensionCommunicationFactory","GetMediaExtensionCommunicationFactory function [Windows API]","comppkgsup/GetMediaExtensionCommunicationFactory","winprog.getmediaextensioncommunicationfactory"]
old-location: winprog\getmediaextensioncommunicationfactory.htm
tech.root: winprog
ms.assetid: 79186891-FD54-4498-AF2A-D79D30F859A2
ms.date: 12/05/2018
ms.keywords: GetMediaExtensionCommunicationFactory, GetMediaExtensionCommunicationFactory function [Windows API], comppkgsup/GetMediaExtensionCommunicationFactory, winprog.getmediaextensioncommunicationfactory
req.header: comppkgsup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comppkgsup.lib
req.dll: CompPkgSup.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetMediaExtensionCommunicationFactory
 - comppkgsup/GetMediaExtensionCommunicationFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CompPkgSup.dll
api_name:
 - GetMediaExtensionCommunicationFactory
---

# GetMediaExtensionCommunicationFactory function


## -description

Creates a communication factory for registering a media extension.

## -parameters

### -param factory [out]

The communication factory.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Use this API to create and hold a reference count on  the communication factory. Once the call to <b>RegisterMediaExtensionForAppService</b> has been made the  reference count on the communication factory can be released.

