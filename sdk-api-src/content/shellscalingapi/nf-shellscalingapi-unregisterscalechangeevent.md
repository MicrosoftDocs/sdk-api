---
UID: NF:shellscalingapi.UnregisterScaleChangeEvent
title: UnregisterScaleChangeEvent function
author: windows-sdk-content
description: Unregisters for the scale change event registered through RegisterScaleChangeEvent. This function replaces RevokeScaleChangeNotifications.
old-location: shell\UnregisterScaleChangeEvent.htm
old-project: shell
ms.assetid: 4BF2F912-857A-4122-A9E1-6704F92240E6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: UnregisterScaleChangeEvent, UnregisterScaleChangeEvent function [Windows Shell], shell.UnregisterScaleChangeEvent, shellscalingapi/UnregisterScaleChangeEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shellscalingapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: SHELL_UI_COMPONENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - shcore.dll
 - API-MS-Win-shcore-scaling-l1-1-1.dll
 - API-MS-Win-ShCore-Scaling-l1-1-2.dll
 - api-ms-win-shcore-scaling-l1.dll
api_name:
 - UnregisterScaleChangeEvent
product: Windows
targetos: Windows
req.lib: Shcore.lib
req.dll: Shcore.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# UnregisterScaleChangeEvent function


## -description


Unregisters for the scale change event registered through <a href="https://msdn.microsoft.com/05FAFC9B-DCB7-464A-9933-7166C7E53D40">RegisterScaleChangeEvent</a>. This function replaces <a href="https://msdn.microsoft.com/95F1D147-D364-4b11-AE2B-CD1FCEA07B5D">RevokeScaleChangeNotifications</a>.


## -parameters




### -param dwCookie [in]

A pointer to the cookie retrieved in the call to <a href="https://msdn.microsoft.com/05FAFC9B-DCB7-464A-9933-7166C7E53D40">RegisterScaleChangeEvent</a>.


## -returns



If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2F214512-704D-41A2-86A6-1EF880CD3DB4">GetScaleFactorForMonitor</a>



<a href="https://msdn.microsoft.com/05FAFC9B-DCB7-464A-9933-7166C7E53D40">RegisterScaleChangeEvent</a>
 

 

