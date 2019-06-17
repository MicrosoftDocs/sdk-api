---
UID: NF:roapi.RoGetApartmentIdentifier
title: RoGetApartmentIdentifier function (roapi.h)
author: windows-sdk-content
description: Gets a unique identifier for the current apartment.
old-location: winrt\rogetapartmentidentifier.htm
tech.root: WinRT
ms.assetid: C10AE81B-21AB-4B0A-9463-A36C7A1893C7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RoGetApartmentIdentifier, RoGetApartmentIdentifier function [Windows Runtime], roapi/RoGetApartmentIdentifier, winrt.rogetapartmentidentifier
ms.topic: function
f1_keywords: ["roapi/RoGetApartmentIdentifier"]
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RoGetApartmentIdentifier function


## -description


Gets a unique identifier for the current apartment.


## -parameters




### -param apartmentIdentifier [out]

A process-unique identifier for the current apartment.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown">IApartmentShutdown</a>



<a href="https://docs.microsoft.com/windows/desktop/api/roapi/nf-roapi-roregisterforapartmentshutdown">RoRegisterForApartmentShutdown</a>



<a href="https://docs.microsoft.com/windows/desktop/api/roapi/nf-roapi-rounregisterforapartmentshutdown">RoUnregisterForApartmentShutdown</a>
 

 

