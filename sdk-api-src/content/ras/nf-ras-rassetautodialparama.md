---
UID: NF:ras.RasSetAutodialParamA
title: RasSetAutodialParamA function (ras.h)
description: The RasSetAutodialParam function sets the value of an AutoDial parameter.
helpviewer_keywords: ["RASADP_ConnectionQueryTimeout","RASADP_DisableConnectionQuery","RASADP_FailedConnectionTimeout","RASADP_LoginSessionDisable","RASADP_SavedAddressesLimit","RasSetAutodialParam","RasSetAutodialParam function [RAS]","RasSetAutodialParamA","RasSetAutodialParamW","_ras_rassetautodialparam","ras/RasSetAutodialParam","ras/RasSetAutodialParamA","ras/RasSetAutodialParamW","rras.rassetautodialparam"]
old-location: rras\rassetautodialparam.htm
tech.root: RRAS
ms.assetid: 76c52494-e8ad-41df-bee6-33d90f24e448
ms.date: 12/05/2018
ms.keywords: RASADP_ConnectionQueryTimeout, RASADP_DisableConnectionQuery, RASADP_FailedConnectionTimeout, RASADP_LoginSessionDisable, RASADP_SavedAddressesLimit, RasSetAutodialParam, RasSetAutodialParam function [RAS], RasSetAutodialParamA, RasSetAutodialParamW, _ras_rassetautodialparam, ras/RasSetAutodialParam, ras/RasSetAutodialParamA, ras/RasSetAutodialParamW, rras.rassetautodialparam
f1_keywords:
- ras/RasSetAutodialParam
dev_langs:
- c++
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasSetAutodialParamW (Unicode) and RasSetAutodialParamA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Rasapi32.dll
api_name:
- RasSetAutodialParam
- RasSetAutodialParamA
- RasSetAutodialParamW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RasSetAutodialParamA function


## -description


The 
<b>RasSetAutodialParam</b> function sets the value of an AutoDial parameter.


## -parameters




### -param arg1 [in]

Specifies the AutoDial parameter to set. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASADP_DisableConnectionQuery"></a><a id="rasadp_disableconnectionquery"></a><a id="RASADP_DISABLECONNECTIONQUERY"></a><dl>
<dt><b>RASADP_DisableConnectionQuery</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvValue</i> parameter points to a <b>DWORD</b> value. If this value is zero (the default), AutoDial displays a dialog box to query the user before creating a connection. If this value is one, and the AutoDial database has the phone-book entry to dial, AutoDial creates a connection without displaying the dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="RASADP_LoginSessionDisable"></a><a id="rasadp_loginsessiondisable"></a><a id="RASADP_LOGINSESSIONDISABLE"></a><dl>
<dt><b>RASADP_LoginSessionDisable</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvValue</i> parameter points to a <b>DWORD</b> value. If this value is one, the system disables all AutoDial connections for the current logon session. If this value is zero (the default), AutoDial connections are enabled. The AutoDial system service changes this value to zero when a new user logs on to the workstation.

</td>
</tr>
<tr>
<td width="40%"><a id="RASADP_SavedAddressesLimit"></a><a id="rasadp_savedaddresseslimit"></a><a id="RASADP_SAVEDADDRESSESLIMIT"></a><dl>
<dt><b>RASADP_SavedAddressesLimit</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvValue</i> parameter points to a <b>DWORD</b> value that indicates the maximum number of addresses that AutoDial stores in the registry. AutoDial first stores addresses that it used to create an AutoDial connection; then it stores addresses that it learned after a RAS connection was created. Addresses written using the 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rassetautodialaddressa">RasSetAutodialAddress</a> function are always saved, and are not included in calculating the limit. The default value is 100.

</td>
</tr>
<tr>
<td width="40%"><a id="RASADP_FailedConnectionTimeout"></a><a id="rasadp_failedconnectiontimeout"></a><a id="RASADP_FAILEDCONNECTIONTIMEOUT"></a><dl>
<dt><b>RASADP_FailedConnectionTimeout</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvValue</i> parameter points to a <b>DWORD</b> value that indicates a time-out value, in seconds. When an AutoDial connection attempt fails, the AutoDial system service disables subsequent attempts to reach the same address for the time-out period. This prevents AutoDial from displaying multiple connection dialog boxes for the same logical request by an application. The default value is five.

</td>
</tr>
<tr>
<td width="40%"><a id="RASADP_ConnectionQueryTimeout"></a><a id="rasadp_connectionquerytimeout"></a><a id="RASADP_CONNECTIONQUERYTIMEOUT"></a><dl>
<dt><b>RASADP_ConnectionQueryTimeout</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvValue</i> parameter points to a <b>DWORD</b> value that indicates a time-out value, in seconds. Before attempting an AutoDial connection, the system will display a dialog asking the user to confirm that the system should dial. The dialog has a countdown timer that terminates the dialog with a "Do not dial" selection if the user takes no action. The <b>DWORD</b> value pointed to by lpvValue specifies the initial time on this countdown timer.

</td>
</tr>
</table>
 


### -param arg2 [out]

Pointer to a buffer that contains the new value for the specified parameter.


### -param arg3 [in]

Specifies the size, in bytes, of the value in the <i>lpvValue</i> buffer.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="https://docs.microsoft.com/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwKey</i> or <i>lpvValue</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The size specified by the <i>dwcbValue</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasgetautodialparama">RasGetAutodialParam</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rassetautodialaddressa">RasSetAutodialAddress</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
 

 

## -remarks

> [!NOTE]
> The ras.h header defines RasSetAutodialParam as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

