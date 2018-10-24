---
UID: NF:shdeprecated.IBrowserService.NavigateToPidl
title: IBrowserService::NavigateToPidl
author: windows-sdk-content
description: Deprecated. Navigates the browser to the location indicated by a pointer to an item identifier list (PIDL).
old-location: shell\IBrowserService_NavigateToPidl.htm
tech.root: shell
ms.assetid: eb329a61-1c1a-49c6-9d5e-ccfc7fd8b10c
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: HLNF_ALLOW_AUTONAVIGATE, HLNF_CALLERUNTRUSTED, HLNF_DISABLEWINDOWRESTRICTIONS, HLNF_EXTERNALNAVIGATE, HLNF_NAVIGATINGBACK, HLNF_NAVIGATINGFORWARD, HLNF_NEWWINDOWSMANAGED, HLNF_TRUSTEDFORACTIVEX, HLNF_TRUSTFIRSTDOWNLOAD, HLNF_UNTRUSTEDFORDOWNLOAD, IBrowserService interface [Windows Shell],NavigateToPidl method, IBrowserService.NavigateToPidl, IBrowserService::NavigateToPidl, NavigateToPidl, NavigateToPidl method [Windows Shell], NavigateToPidl method [Windows Shell],IBrowserService interface, SHHLNF_NOAUTOSELECT, SHHLNF_WRITENOHISTORY, shdeprecated/IBrowserService::NavigateToPidl, shell.IBrowserService_NavigateToPidl, zone_IBrowserService_NavigateToPidl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
 - Shdeprecated.h
api_name:
 - IBrowserService.NavigateToPidl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# IBrowserService::NavigateToPidl


## -description


Deprecated. Navigates the browser to the location indicated by a pointer to an item identifier list (PIDL).


## -parameters




### -param pidl [in]

Type: <b>LPCITEMIDLIST</b>

The PIDL of the location.


### -param grfHLNF [in]

Type: <b>DWORD</b>

One or more of the following flags.



#### HLNF_NAVIGATINGBACK (0x00000004)

The navigation is to the previous destination in the browse context.



#### HLNF_NAVIGATINGFORWARD (0x00000008)

The navigation is to the next destination in the browse context.



#### HLNF_CALLERUNTRUSTED (0x00200000)

The navigation was possibly initiated through a webpage by scripting code already on the system.



#### HLNF_TRUSTEDFORACTIVEX (0x00400000)

The navigation allows Microsoft ActiveX prompts.



#### HLNF_DISABLEWINDOWRESTRICTIONS (0x00800000)

A new window is created by a URL in a zone with window restrictions security mitigation disabled.



#### HLNF_TRUSTFIRSTDOWNLOAD (0x01000000)

The new window is the result of a user-initiated action. If the destination attempts a download on entry, it should be trusted.



#### HLNF_UNTRUSTEDFORDOWNLOAD (0x02000000)

Microsoft Internet Explorer is navigating to an untrusted non-HTML file. Do not download the file.



#### HLNF_EXTERNALNAVIGATE (0x10000000)



#### HLNF_ALLOW_AUTONAVIGATE (0x20000000)



#### HLNF_NEWWINDOWSMANAGED (0x80000000)

If this navigation results in a new window, it should be subject to Pop-up Manager.



#### SHHLNF_WRITENOHISTORY (0x08000000)

The destination of the current navigation should not be placed into the browser's history record.



#### SHHLNF_NOAUTOSELECT (0x04000000)

The destination of the current navigation should not be automatically selected from the browser's history record.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/e12ada84-0825-4946-8075-731dfc51ef50">IBrowserService</a>



<a href="https://msdn.microsoft.com/71f99bc7-0601-4dc4-90df-c9f9a0ab51a5">_NavigateToPidl</a>
 

 

