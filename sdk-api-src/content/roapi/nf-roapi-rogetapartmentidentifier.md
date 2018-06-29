---
UID: NF:roapi.RoGetApartmentIdentifier
title: RoGetApartmentIdentifier function
author: windows-sdk-content
description: Gets a unique identifier for the current apartment.
old-location: winrt\rogetapartmentidentifier.htm
old-project: WinRT
ms.assetid: C10AE81B-21AB-4B0A-9463-A36C7A1893C7
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: RoGetApartmentIdentifier, RoGetApartmentIdentifier function [Windows Runtime], roapi/RoGetApartmentIdentifier, winrt.rogetapartmentidentifier
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: roapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: RO_INIT_TYPE
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
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
req.product: ADAM
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




<a href="https://msdn.microsoft.com/28EDAC77-5175-4AF7-A06C-B735336AAD9B">IApartmentShutdown</a>



<a href="https://msdn.microsoft.com/DE0C79AD-D80F-44EE-A628-147FC8474905">RoRegisterForApartmentShutdown</a>



<a href="https://msdn.microsoft.com/B6E22C50-14EC-4B0F-8C97-7D1062BF6072">RoUnregisterForApartmentShutdown</a>
 

 

