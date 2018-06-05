---
UID: NF:wpcapi.IWPCProviderConfig.RequestOverride
title: IWPCProviderConfig::RequestOverride
author: windows-sdk-content
description: Called for the current provider to enable configuration override.
old-location: parcon\iwpcproviderconfig_requestoverride.htm
old-project: parcon
ms.assetid: 66A75879-9A95-472A-9529-61A57E37B9A0
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IWPCProviderConfig interface,RequestOverride method, IWPCProviderConfig.RequestOverride, IWPCProviderConfig::RequestOverride, RequestOverride, RequestOverride method, RequestOverride method,IWPCProviderConfig interface, WPCFLAG_APPS_RESTRICTED, WPCFLAG_GAMES_BLOCKED, WPCFLAG_HOURS_RESTRICTED, WPCFLAG_LOGGING_REQUIRED, WPCFLAG_NO_RESTRICTION, WPCFLAG_WEB_FILTERED, parcon.iwpcproviderconfig_requestoverride, wpcapi/IWPCProviderConfig::RequestOverride
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wpcapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wpcprovider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wpcapi.h
api_name:
-	IWPCProviderConfig.RequestOverride
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWPCProviderConfig::RequestOverride


## -description


Called for the current provider to enable configuration override.


## -parameters




### -param hWnd [in]

A handle to the parent window.


### -param bstrPath [in]

Pointer to a string that contains the path.


### -param dwFlags [in]

Flags that specify the restriction. This can be one of more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WPCFLAG_NO_RESTRICTION"></a><a id="wpcflag_no_restriction"></a><dl>
<dt><b>WPCFLAG_NO_RESTRICTION</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
There are no restrictions.

</td>
</tr>
<tr>
<td width="40%"><a id="WPCFLAG_LOGGING_REQUIRED"></a><a id="wpcflag_logging_required"></a><dl>
<dt><b>WPCFLAG_LOGGING_REQUIRED</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Activity logging is on.

</td>
</tr>
<tr>
<td width="40%"><a id="WPCFLAG_WEB_FILTERED"></a><a id="wpcflag_web_filtered"></a><dl>
<dt><b>WPCFLAG_WEB_FILTERED</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
A Web Content Filter is active.

</td>
</tr>
<tr>
<td width="40%"><a id="WPCFLAG_HOURS_RESTRICTED"></a><a id="wpcflag_hours_restricted"></a><dl>
<dt><b>WPCFLAG_HOURS_RESTRICTED</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
Hours are restricted.

</td>
</tr>
<tr>
<td width="40%"><a id="WPCFLAG_GAMES_BLOCKED"></a><a id="wpcflag_games_blocked"></a><dl>
<dt><b>WPCFLAG_GAMES_BLOCKED</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
Games are blocked.

</td>
</tr>
<tr>
<td width="40%"><a id="WPCFLAG_APPS_RESTRICTED"></a><a id="wpcflag_apps_restricted"></a><dl>
<dt><b>WPCFLAG_APPS_RESTRICTED</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
Applications are restricted.

</td>
</tr>
</table>
 


## -returns



If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/008786aa-72ef-4591-8826-01176d3e3fba">IWPCProviderConfig</a>
 

 

