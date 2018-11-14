---
UID: NF:wpcapi.IWPCWebSettings.RequestURLOverride
title: IWPCWebSettings::RequestURLOverride
author: windows-sdk-content
description: Requests that the Parental Controls web restrictions subsystem set the specified primary and sub URLs to the allowed state.
old-location: parcon\iwpcwebsettings_requesturloverride.htm
tech.root: parcon
ms.assetid: 2e229b0e-59ae-4fcf-a398-32bc20611802
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWPCWebSettings interface,RequestURLOverride method, IWPCWebSettings.RequestURLOverride, IWPCWebSettings::RequestURLOverride, RequestURLOverride, RequestURLOverride method, RequestURLOverride method,IWPCWebSettings interface, parcon.iwpcwebsettings_requesturloverride, wpcapi/IWPCWebSettings::RequestURLOverride
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wpcapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWPCWebSettings.RequestURLOverride
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wpcapi.h
: 
- IWPCWebSettings.RequestURLOverride
: 
---

# IWPCWebSettings::RequestURLOverride


## -description


Requests that the Parental Controls web restrictions subsystem set the specified primary and sub URLs to the allowed state.


## -parameters




### -param hWnd [in]

A handle to the parent window. This is  needed for proper User Account Control (UAC) dialog box behavior.


### -param pcszURL [in]

A pointer to primary URL for override.


### -param cURLs [in]

The number of entries in <i>ppcszSubURLs</i>.


### -param ppcszSubURLs [in]

Pointers to URLs that include pages with the primary URL.


### -param pfChanged [out]

Pointer to flag notifying completion of override changed status. This parameter is 1 if the status is changed, and 0 otherwise.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/80629db8-0040-4545-a313-5cf7aa3d7f8b">IWPCWebSettings</a>
 

 

