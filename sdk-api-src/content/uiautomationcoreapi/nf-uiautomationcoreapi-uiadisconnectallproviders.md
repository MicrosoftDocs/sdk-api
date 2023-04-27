---
UID: NF:uiautomationcoreapi.UiaDisconnectAllProviders
title: UiaDisconnectAllProviders function (uiautomationcoreapi.h)
description: Releases all Microsoft UI Automation resources that are held by all providers associated with the calling process.
helpviewer_keywords: ["UiaDisconnectAllProviders","UiaDisconnectAllProviders function [Windows Accessibility]","uiautomationcoreapi/UiaDisconnectAllProviders","winauto.uiauto_UiaDisconnectAllProviders"]
old-location: winauto\uiauto_UiaDisconnectAllProviders.htm
tech.root: WinAuto
ms.assetid: 1E46DC9A-8E72-49B2-B867-C075962EF00A
ms.date: 12/05/2018
ms.keywords: UiaDisconnectAllProviders, UiaDisconnectAllProviders function [Windows Accessibility], uiautomationcoreapi/UiaDisconnectAllProviders, winauto.uiauto_UiaDisconnectAllProviders
req.header: uiautomationcoreapi.h
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
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UiaDisconnectAllProviders
 - uiautomationcoreapi/UiaDisconnectAllProviders
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
 - Ext-MS-Win-uiacore-l1-1-0.dll
 - Ext-MS-Win-UIaCore-l1-1-2.dll
 - Ext-MS-Win-UiaCore-L1-1-3.dll
api_name:
 - UiaDisconnectAllProviders
---

# UiaDisconnectAllProviders function


## -description

Releases all Microsoft UI Automation resources that are held by all providers associated with the calling process.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A provider application should use this function to release UI Automation resources before shutting down.

This function cannot be called in response to a call to the <a href="/windows/desktop/DevNotes/-sendmessage">SendMessage</a> function. An application cannot make outbound Component Object Model (COM) calls in response to a call to <b>SendMessage</b>, and releasing a provider is typically an outbound COM call.  The <b>UiaDisconnectAllProviders</b> function returns RPC_E_CANTCALLOUT_ININPUTSYNCCALL if the function is called in response to a <b>SendMessage</b> call.  You can use the <a href="/windows/desktop/api/winuser/nf-winuser-insendmessageex">InSendMessageEx</a> function to determine whether a particular message is being handled in response to a <b>SendMessage</b> call.


An application that calls <b>UiaDisconnectAllProviders</b> should not respond to a re-entrant [WM_GETOBJECT](/windows/win32/winauto/wm-getobject) message by returning a pointer to the provider that it is trying to disconnect.  If the application tries to disconnect a provider, but then calls the <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiareturnrawelementprovider">UiaReturnRawElementProvider</a> function with that same provider during the disconnect attempt, the provider might not be fully disconnected.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-functions">Functions for Providers</a>



<a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiadisconnectprovider">UiaDisconnectProvider</a>
