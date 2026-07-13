---
UID: NF:ras.RasDialW
title: RasDialW function (ras.h)
description: The RasDial function establishes a RAS connection between a RAS client and a RAS server. The connection data includes callback and user-authentication information. (Unicode)
helpviewer_keywords: ["0", "1", "2", "RasDial", "RasDial function [RAS]", "RasDialW", "_ras_rasdial", "ras/RasDial", "ras/RasDialW", "rras.rasdial"]
old-location: rras\rasdial.htm
tech.root: RRAS
ms.assetid: 579a9038-8216-4948-a065-fd45b97da73a
ms.date: 12/05/2018
ms.keywords: 0, 1, 2, RasDial, RasDial function [RAS], RasDialA, RasDialW, _ras_rasdial, ras/RasDial, ras/RasDialA, ras/RasDialW, rras.rasdial
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasDialW (Unicode) and RasDialA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasDialW
 - ras/RasDialW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ras-rasapi32-l1-1-2.dll
 - Rasapi32.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-0.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-1.dll
api_name:
 - RasDial
 - RasDialA
 - RasDialW
---

# RasDialW function


## -description

The 
<b>RasDial</b> function establishes a RAS connection between a RAS client and a RAS server. The connection data includes callback and user-authentication information.

## -parameters

### -param unnamedParam1 [in]

Pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)">RASDIALEXTENSIONS</a> structure that specifies a set of 
<b>RasDial</b> extended features to enable. Set this parameter to <b>NULL</b> if there is not a need to enable these features.

### -param unnamedParam2 [in]

Pointer to a null-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box.

### -param unnamedParam3 [in]

Pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)">RASDIALPARAMS</a> structure that specifies calling parameters for the RAS connection. Use the 
<a href="/windows/desktop/api/ras/nf-ras-rasgetentrydialparamsa">RasGetEntryDialParams</a> function to retrieve a copy of this structure for a particular phone-book entry. 




The caller must set the 
<a href="/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)">RASDIALPARAMS</a> structure's <b>dwSize</b> member to sizeof(<b>RASDIALPARAMS</b>) to identify the version of the structure being passed.

If the <b>szPhoneNumber</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)">RASDIALPARAMS</a> structure is an empty string, 
<b>RasDial</b> uses the phone number stored in the phone-book entry.

### -param unnamedParam4 [in]

Specifies the nature of the <i>lpvNotifier</i> parameter. If <i>lpvNotifier</i> is <b>NULL</b>, <i>dwNotifierType</i> is ignored. If <i>lpvNotifier</i> is not <b>NULL</b>, set <i>dwNotifierType</i> to one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvNotifier</i> parameter points to a 
<a href="/windows/desktop/api/ras/nc-ras-rasdialfunc">RasDialFunc</a> callback function.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvNotifier</i> parameter points to a 
<a href="/windows/desktop/api/ras/nc-ras-rasdialfunc1">RasDialFunc1</a> callback function.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvNotifier</i> parameter points to a 
<a href="/windows/desktop/api/ras/nc-ras-rasdialfunc2">RasDialFunc2</a> callback function. 

</td>
</tr>
</table>

### -param unnamedParam5 [in]

Specifies a window handle or a 
<a href="/windows/desktop/api/ras/nc-ras-rasdialfunc">RasDialFunc</a>, 
<a href="/windows/desktop/api/ras/nc-ras-rasdialfunc1">RasDialFunc1</a>, or 
<a href="/windows/desktop/api/ras/nc-ras-rasdialfunc2">RasDialFunc2</a> callback function to receive 
<b>RasDial</b> event notifications. The <i>dwNotifierType</i> parameter specifies the nature of <i>lpvNotifier</i>. Please refer to its description preceding for further detail. 




If this parameter is not <b>NULL</b>, 
<b>RasDial</b> sends the window a message, or calls the callback function, for each 
<b>RasDial</b> event. Additionally, the 
<b>RasDial</b> call operates asynchronously: 
<b>RasDial</b> returns immediately, before the connection is established, and communicates its progress via the window or callback function.

If <i>lpvNotifier</i> is <b>NULL</b>, the 
<b>RasDial</b> call operates synchronously: 
<b>RasDial</b> does not return until the connection attempt has completed successfully or failed.

If <i>lpvNotifier</i> is not <b>NULL</b>, notifications to the window or callback function can occur at any time after the initial call to 
<b>RasDial</b>. Notifications end when one of the following events occurs:

<ul>
<li>The connection is established. In other words, the RAS connection state is RASCS_Connected.</li>
<li>The connection fails. In other words, <i>dwError</i> is nonzero.</li>
<li>
<a href="/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a> is called on the connection.</li>
</ul>
The callback notifications are made in the context of a thread captured during the initial call to 
<b>RasDial</b>.

### -param unnamedParam6 [out]

Pointer to a variable of type <b>HRASCONN</b>. Set the <b>HRASCONN</b> variable to <b>NULL</b> before calling 
<b>RasDial</b>. If 
<b>RasDial</b> succeeds, it stores a handle to the RAS connection into <i>*lphRasConn</i>.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b> and a handle to the RAS connection is returned in the variable pointed to by <i>lphRasConn</i>.

If the function fails, the return value is from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

## -remarks

Errors that occur after the immediate return can be detected by 
<a href="/windows/desktop/api/ras/nf-ras-rasgetconnectstatusa">RasGetConnectStatus</a>. Data is available until an application calls 
<a href="/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a> to hang up the connection.

An application must eventually call 
<a href="/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a> whenever a non-<b>NULL</b> connection handle is stored into *<i>lphRasConn</i>. This applies even if 
<b>RasDial</b> returns a nonzero (error) value.

An application can safely call 
<a href="/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a> from a 
<b>RasDial</b> notifier callback function. If this is done, however, the hang-up does not occur until the routine returns.

If the structure pointed to by <i>lpRasDialExtensions</i> enables <b>RDEOPT_PausedStates</b>, the 
<b>RasDial</b> function pauses whenever it enters a state in which the <b>RASCS_PAUSED</b> bit is set to one. To restart 
<b>RasDial</b> from such a paused state, call 
<b>RasDial</b> again, passing the connection handle returned from the original 
<b>RasDial</b> call in <i>*lphRasConn</i>. The same notifier used in the original 
<b>RasDial</b> call must be used when restarting from a paused state.

The <i>lpvNotifier</i> parameter is a handle to a window to receive progress notification messages. In a progress notification message, <i>wParam</i> is the equivalent of the <i>rasconnstate</i> parameter of 
<a href="/windows/desktop/api/ras/nc-ras-rasdialfunc">RasDialFunc</a> and 
<a href="/windows/desktop/api/ras/nc-ras-rasdialfunc1">RasDialFunc1</a>, and <i>lParam</i> is the equivalent of the <i>dwError</i> parameter of 
<b>RasDialFunc</b> and 
<b>RasDialFunc1</b>. 




The progress notification message uses a system registered message code. You can obtain the value of this message code as follows:


```cpp
UINT unMsg = RegisterWindowMessageA( RASDIALEVENT );
if (unMsg == 0)
    unMsg = WM_RASDIALEVENT;

```


RAS supports referenced connections. If the entry being dialed is already connected, 
<b>RasDial</b>  returns <b>SUCCESS</b> and the connection is referenced. To disconnect the connection, each 
<b>RasDial</b> on the connection should be matched by a 
<a href="/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a>.

Because some phone-book entries require Extensible Authentication Protocol (EAP) for authentication, the caller should call 
<a href="/windows/desktop/api/ras/nf-ras-rasgeteapuseridentitya">RasGetEapUserIdentity</a> before calling 
<b>RasDial</b>. If 
<b>RasGetEapUserIdentity</b> returns <b>ERROR_INVALID_FUNCTION_FOR_ENTRY</b>, the phone-book entry does not require EAP. However, if 
<b>RasGetEapUserIdentity</b> returns NO_ERROR, the caller should copy the EAP identity information from 
<b>RasGetEapUserIdentity</b> into the <b>RasEapInfo</b> member of 
<a href="/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)">RASDIALEXTENSIONS</a>, and the <b>szUserName</b> member of 
<a href="/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)">RASDIALPARAMS</a>. See 
<b>RasGetEapUserIdentity</b> for more information. If the phone-book entry requires EAP, the <b>dwfOptions</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a> structure for the entry contains the <b>RASEO_RequireEAP</b> flag.

To specify that 
<b>RasDial</b> should enter a <b>RASCS_CallbackSetByCaller</b> state, set <i>lpRasDialParams</i>-&gt;<b>szCallbackNumber</b> to "*" on the initial call to 
<b>RasDial</b>. When the notification handler is called with this state, set the callback number to a number supplied by the user.





> [!NOTE]
> The ras.h header defines RasDial as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/address-ovr">Dialable Addresses</a>



<a href="/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)">RASDIALEXTENSIONS</a>



<a href="/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)">RASDIALPARAMS</a>



<a href="/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga">RasDialDlg</a>



<a href="/windows/desktop/api/ras/nc-ras-rasdialfunc">RasDialFunc</a>



<a href="/windows/desktop/api/ras/nc-ras-rasdialfunc1">RasDialFunc1</a>



<a href="/windows/desktop/api/ras/nc-ras-rasdialfunc2">RasDialFunc2</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetconnectstatusa">RasGetConnectStatus</a>



<a href="/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>



<a href="/windows/desktop/RRAS/virtual-private-network-connections">Virtual Private Network Connections</a>



<a href="/windows/desktop/RRAS/wm-rasdialevent">WM_RASDIALEVENT</a>
