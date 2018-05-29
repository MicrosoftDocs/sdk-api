---
UID: NF:winwlx.WlxWkstaLockedSAS
title: WlxWkstaLockedSAS function
author: windows-sdk-content
description: Winlogon calls this function when it receives a secure attention sequence (SAS) and the workstation is locked.
old-location: security\wlxwkstalockedsas.htm
old-project: SecAuthN
ms.assetid: 7a9f8b00-857a-432e-bb49-2251504c46a0
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: WLX_SAS_TYPE_CTRL_ALT_DEL, WLX_SAS_TYPE_SC_INSERT, WLX_SAS_TYPE_SC_REMOVE, WLX_SAS_TYPE_TIMEOUT, WlxWkstaLockedSAS, WlxWkstaLockedSAS function [Security], _gina_wlxwkstalockedsas, security.wlxwkstalockedsas, winwlx/WlxWkstaLockedSAS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winwlx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ICONINFOEXW, *PICONINFOEXW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Winwlx.h
api_name:
-	WlxWkstaLockedSAS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlxWkstaLockedSAS function


## -description



			The <b>WlxWkstaLockedSAS</b> function must be implemented by a replacement <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a> calls this function when it receives a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">secure attention sequence</a> (SAS) and the workstation is locked. The GINA should return a value that indicates the workstation is to remain locked, the workstation is to be unlocked, or the logged-on user is to be logged off (which leaves the workstation locked until the logoff is completed).
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param pWlxContext [in]

A pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> for this station.


### -param dwSasType [in]

Specifies the type of SAS that occurred. Values from zero to WLX_SAS_TYPE_MAX_MSFT_VALUE are reserved for standard Microsoft SAS types. GINA developers can use values greater than WLX_SAS_TYPE_MAX_MSFT_VALUE to define additional SAS types.

The following SAS types are predefined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_TYPE_CTRL_ALT_DEL"></a><a id="wlx_sas_type_ctrl_alt_del"></a><dl>
<dt><b>WLX_SAS_TYPE_CTRL_ALT_DEL</b></dt>
</dl>
</td>
<td width="60%">
Indicates a user has typed the standard CTRL+ALT+DEL <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">secure attention sequence</a> (SAS).

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_TYPE_SC_INSERT"></a><a id="wlx_sas_type_sc_insert"></a><dl>
<dt><b>WLX_SAS_TYPE_SC_INSERT</b></dt>
</dl>
</td>
<td width="60%">
Indicates that a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> has been inserted into a compatible device.

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_TYPE_SC_REMOVE"></a><a id="wlx_sas_type_sc_remove"></a><dl>
<dt><b>WLX_SAS_TYPE_SC_REMOVE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that a smart card has been removed from a compatible device.

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_TYPE_TIMEOUT"></a><a id="wlx_sas_type_timeout"></a><dl>
<dt><b>WLX_SAS_TYPE_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
Indicates that no user input was received within the specified time-out period.

</td>
</tr>
</table>
 


## -returns




						The <b>WlxWkstaLockedSAS</b> function should return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_NONE</b></dt>
</dl>
</td>
<td width="60%">
Tells <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a> to keep the workstation locked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_FORCE_LOGOFF</b></dt>
</dl>
</td>
<td width="60%">
Tells Winlogon to forcibly log the user off.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_LOGOFF</b></dt>
</dl>
</td>
<td width="60%">
Tells Winlogon to log the current user off.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_UNLOCK_WKSTA</b></dt>
</dl>
</td>
<td width="60%">
Tells Winlogon to unlock the workstation.

</td>
</tr>
</table>
 




## -remarks



Before calling <b>WlxWkstaLockedSAS</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.




## -see-also




<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 

