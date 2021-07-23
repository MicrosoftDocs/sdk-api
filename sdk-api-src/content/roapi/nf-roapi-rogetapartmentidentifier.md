---
UID: NF:roapi.RoGetApartmentIdentifier
title: RoGetApartmentIdentifier function (roapi.h)
description: Gets a unique identifier for the current apartment.
helpviewer_keywords: ["RoGetApartmentIdentifier","RoGetApartmentIdentifier function [Windows Runtime]","roapi/RoGetApartmentIdentifier","winrt.rogetapartmentidentifier"]
old-location: winrt\rogetapartmentidentifier.htm
tech.root: WinRT
ms.assetid: C10AE81B-21AB-4B0A-9463-A36C7A1893C7
ms.date: 12/05/2018
ms.keywords: RoGetApartmentIdentifier, RoGetApartmentIdentifier function [Windows Runtime], roapi/RoGetApartmentIdentifier, winrt.rogetapartmentidentifier
req.header: roapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RoGetApartmentIdentifier
 - roapi/RoGetApartmentIdentifier
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComBase.dll
 - API-MS-Win-Core-WinRT-l1-1-0.dll
api_name:
 - RoGetApartmentIdentifier
---

# RoGetApartmentIdentifier function


## -description

Gets a unique identifier for the current apartment.

## -parameters

### -param apartmentIdentifier [out]

A process-unique identifier for the current apartment.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown">IApartmentShutdown</a>



<a href="/windows/desktop/api/roapi/nf-roapi-roregisterforapartmentshutdown">RoRegisterForApartmentShutdown</a>



<a href="/windows/desktop/api/roapi/nf-roapi-rounregisterforapartmentshutdown">RoUnregisterForApartmentShutdown</a>