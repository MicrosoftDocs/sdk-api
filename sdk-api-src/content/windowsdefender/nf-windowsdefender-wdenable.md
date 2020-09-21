---
UID: NF:windowsdefender.WDEnable
title: WDEnable function (windowsdefender.h)
description: Changes Windows Defender status to on or off.
helpviewer_keywords: ["WDEnable","WDEnable function [Legacy Windows Environment Features]","lwef.defender_wdenable","shell.defender_wdenable","shell_defender_WDEnable","windowsdefender/WDEnable"]
old-location: lwef\defender_wdenable.htm
tech.root: lwef
ms.assetid: a12d3b2a-6873-4ef4-90d6-08dbd5feb959
ms.date: 12/05/2018
ms.keywords: WDEnable, WDEnable function [Legacy Windows Environment Features], lwef.defender_wdenable, shell.defender_wdenable, shell_defender_WDEnable, windowsdefender/WDEnable
req.header: windowsdefender.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: MpClient.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WDEnable
 - windowsdefender/WDEnable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - MpClient.dll
api_name:
 - WDEnable
---

# WDEnable function


## -description

Changes Windows Defender status to on or off. 


<div class="alert"><b>Note</b>  <p class="note"><b>WDEnable</b> is no longer available for use as of Windows 10, version 1607. 

<p class="note">Beginning in Windows 10, version 1607 and Windows Server 2016, the <b>WDEnable</b> function always returns <b>E_NOTIMPL</b>.

</div>
<div> </div>

## -parameters

### -param fEnable [in]

Type: <b>BOOL</b>

Windows Defender status that the calling application wants to set. <b>TRUE</b> enables Windows Defender. <b>FALSE</b> disables Windows Defender.

## -returns

Type: <b>HRESULT</b>

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Windows Defender is configured to the state requested. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Calling application does not have sufficient permission or is flagged as a threat by Windows Defender signature database.

Calling application identity is not verifiable through digital signing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ACCESS_DISABLED_BY_POLICY)</b></dt>
</dl>
</td>
<td width="60%">
Calling application request contradicts with the Windows Defender status set by group policy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>

## -remarks

The application calling this function must run with administrator permissions on the local computer.  Windows Defender also validates (1) the proper signing of the calling process and all loaded modules and (2) that the IMAGE_DLLCHARACTERISTICS_FORCE_INTEGRITY flag is set on the calling process and all loaded modules before allowing the calling application to change the status. If the calling process image (or any loaded modules) is not signed or is flagged as a threat by the Windows Defender signature, then the call fails with the appropriate error code.

## -see-also

<a href="/windows/desktop/api/windowsdefender/nf-windowsdefender-wdstatus">WDStatus</a>