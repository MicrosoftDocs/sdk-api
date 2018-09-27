---
UID: NF:uiautomationcoreapi.UiaDisconnectProvider
title: UiaDisconnectProvider function
author: windows-sdk-content
description: Releases all references that a particular provider holds to Microsoft UI Automation objects.
old-location: winauto\uiauto_UiaDisconnectProvider.htm
tech.root: WinAuto
ms.assetid: D4CE0071-47C4-421D-A0F1-D6E2D9983838
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: UiaDisconnectProvider, UiaDisconnectProvider function [Windows Accessibility], uiautomationcoreapi/UiaDisconnectProvider, winauto.uiauto_UiaDisconnectProvider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
 - Ext-MS-Win-uiacore-l1-1-0.dll
 - Ext-MS-Win-UIaCore-l1-1-1.dll
 - Ext-MS-Win-UIaCore-l1-1-2.dll
 - Ext-MS-Win-UiaCore-L1-1-3.dll
api_name:
 - UiaDisconnectProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaDisconnectProvider function


## -description


Releases all references that a particular provider holds to Microsoft UI Automation objects.


## -parameters




### -param pProvider [in]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>*</b>

The provider to be disconnected.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A provider should call this function to clean up UI Automation resources that are associated with a UI element that was destroyed.  The DLL  associated with the UI element can be safely unloaded after the function returns.

After this function returns, all client requests that are associated with the disconnected provider receive the <a href="https://msdn.microsoft.com/en-us/library/Ee671218(v=VS.85).aspx">UIA_E_ELEMENTNOTAVAILABLE</a> 
error code.

This function cannot be called in response to a call to the <a href="https://msdn.microsoft.com/aed898b3-bb48-4da2-aee7-834ae65a2d51">SendMessage</a> function. An application cannot make outbound Component Object Model (COM) calls in response to a call to <b>SendMessage</b>, and releasing a provider is typically an outbound COM call.  The <b>UiaDisconnectProvider</b> function returns RPC_E_CANTCALLOUT_ININPUTSYNCCALL if the function is called in response to a <b>SendMessage</b> call.  You can use the <a href="https://msdn.microsoft.com/en-us/library/ms644942(v=VS.85).aspx">InSendMessageEx</a> function to determine whether a particular message is being handled in response to a <b>SendMessage</b> call.

For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=231683">BUG: RPC_E_CANTCALLOUT_ININPUTSYNCCALL Error When System Menu Is Shown in Taskbar</a> on the MSDN Support website.

An application that calls <b>UiaDisconnectProvider</b> should not respond to a re-entrant <a href="https://msdn.microsoft.com/59350aa1-1697-4110-b9a6-f30ee56c4cff">WM_GETOBJECT</a> message by returning a pointer to the provider that it is trying to disconnect.  If the application tries to disconnect a provider, but then calls the <a href="https://msdn.microsoft.com/800dfad2-2263-4069-a1fe-f737842b3357">UiaReturnRawElementProvider</a> function with that same provider during the disconnect attempt, the provider might not be fully disconnected.




## -see-also




<a href="https://msdn.microsoft.com/76012ec7-0114-4b6b-a35e-5cfde5b90230">Functions for Providers</a>



<a href="https://msdn.microsoft.com/1E46DC9A-8E72-49B2-B867-C075962EF00A">UiaDisconnectAllProviders</a>
 

 

