---
UID: NF:roparameterizediid.RoFreeParameterizedTypeExtra
title: RoFreeParameterizedTypeExtra function (roparameterizediid.h)
author: windows-sdk-content
description: Frees the handle allocated by RoGetParameterizedTypeInstanceIID.
old-location: winrt\rofreeparameterizedtypeextra.htm
tech.root: WinRT
ms.assetid: A9A063F3-D6E0-4383-B9AD-EA115FC3A8FD
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RoFreeParameterizedTypeExtra, RoFreeParameterizedTypeExtra function [Windows Runtime], roparameterizediid/RoFreeParameterizedTypeExtra, winrt.rofreeparameterizedtypeextra
ms.topic: function
req.header: roparameterizediid.h
req.include-header: Paraminstanceapi.h
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
req.lib: Runtimeobject.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - runtimeobject.lib
 - runtimeobject.dll
 - API-MS-Win-Core-WinRT-roparameterizediid-l1-1-0.dll
 - ComBase.dll
api_name:
 - RoFreeParameterizedTypeExtra
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RoFreeParameterizedTypeExtra function


## -description


Frees the handle allocated by <a href="https://msdn.microsoft.com/DE908C82-5D7C-415C-B08B-31786589979B">RoGetParameterizedTypeInstanceIID</a>.


## -parameters




### -param extra [in]

Type: <b>ROPARAMIIDHANDLE</b>

A handle to the IID.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



