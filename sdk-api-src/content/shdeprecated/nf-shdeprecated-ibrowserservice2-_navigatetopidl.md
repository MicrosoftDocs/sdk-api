---
UID: NF:shdeprecated.IBrowserService2._NavigateToPidl
title: IBrowserService2::_NavigateToPidl
author: windows-sdk-content
description: Deprecated. Navigates the base class to a new location synchronously.
old-location: shell\IBrowserService2__NavigateToPidl.htm
old-project: shell
ms.assetid: 71f99bc7-0601-4dc4-90df-c9f9a0ab51a5
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: HLNF_ALLOW_AUTONAVIGATE, HLNF_CALLERUNTRUSTED, HLNF_DISABLEWINDOWRESTRICTIONS, HLNF_EXTERNALNAVIGATE, HLNF_NEWWINDOWSMANAGED, HLNF_TRUSTEDFORACTIVEX, HLNF_TRUSTFIRSTDOWNLOAD, HLNF_UNTRUSTEDFORDOWNLOAD, IBrowserService2 interface [Windows Shell],_NavigateToPidl method, IBrowserService2._NavigateToPidl, IBrowserService2::_NavigateToPidl, SHHLNF_NOAUTOSELECT, SHHLNF_WRITENOHISTORY, _NavigateToPidl, _NavigateToPidl method [Windows Shell], _NavigateToPidl method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_NavigateToPidl, shell.IBrowserService2__NavigateToPidl, zone_IBrowserService2__NavigateToPidl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BNSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shdeprecated.h
api_name:
-	IBrowserService2._NavigateToPidl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_NavigateToPidl


## -description


Deprecated. Navigates the base class to a new location synchronously.


## -parameters




### -param pidl [in]

Type: <b>LPCITEMIDLIST</b>

The PIDL identifying the new location.


### -param grfHLNF [in]

Type: <b>DWORD</b>

The value or values from the <a href="_inet_HLNF_Enumerated_Type_cpp">HLNF</a> enumeration. The following values are also supported.



#### HLNF_CALLERUNTRUSTED

0x00200000. The navigation was possibly initiated through a webpage by scripting code already on the system.



#### HLNF_TRUSTEDFORACTIVEX

0x00400000. The navigation allows ActiveX prompts.



#### HLNF_DISABLEWINDOWRESTRICTIONS

0x00800000. The new window is created by a URL in a zone that has the window restrictions security mitigation disabled.



#### HLNF_TRUSTFIRSTDOWNLOAD

0x01000000. The new window is the result of a user-initiated action. If the destination attempts a download on entry, it should be trusted.



#### HLNF_UNTRUSTEDFORDOWNLOAD

0x02000000. Internet Explorer is navigating to an untrusted non-HTML file. Do not download the file.



#### SHHLNF_NOAUTOSELECT

0x04000000. This navigation should not automatically select the history folder.



#### SHHLNF_WRITENOHISTORY

0x08000000. This navigation should not be recorded in the history.



#### HLNF_EXTERNALNAVIGATE

0x10000000.



#### HLNF_ALLOW_AUTONAVIGATE

0x20000000.



#### HLNF_NEWWINDOWSMANAGED

0x80000000. If this navigation results in a new window, the new window should be subject to the Pop-up Manager.


### -param dwFlags [in]

Type: <b>DWORD</b>

Not used.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5c100b60-ef2e-4044-9f06-c1d01bcd88d2">IBrowserService2</a>



<a href="https://msdn.microsoft.com/eb329a61-1c1a-49c6-9d5e-ccfc7fd8b10c">NavigateToPidl</a>
 

 

