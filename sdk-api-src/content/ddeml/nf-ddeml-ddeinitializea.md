---
UID: NF:ddeml.DdeInitializeA
title: DdeInitializeA function (ddeml.h)
description: Registers an application with the Dynamic Data Exchange Management Library (DDEML). An application must call this function before calling any other Dynamic Data Exchange Management Library (DDEML) function. (ANSI)
helpviewer_keywords: ["APPCLASS_MONITOR", "APPCLASS_STANDARD", "APPCMD_CLIENTONLY", "APPCMD_FILTERINITS", "CBF_FAIL_ADVISES", "CBF_FAIL_ALLSVRXACTIONS", "CBF_FAIL_CONNECTIONS", "CBF_FAIL_EXECUTES", "CBF_FAIL_POKES", "CBF_FAIL_REQUESTS", "CBF_FAIL_SELFCONNECTIONS", "CBF_SKIP_ALLNOTIFICATIONS", "CBF_SKIP_CONNECT_CONFIRMS", "CBF_SKIP_DISCONNECTS", "CBF_SKIP_REGISTRATIONS", "CBF_SKIP_UNREGISTRATIONS", "DdeInitializeA", "MF_CALLBACKS", "MF_CONV", "MF_ERRORS", "MF_HSZ_INFO", "MF_LINKS", "MF_POSTMSGS", "MF_SENDMSGS", "ddeml/DdeInitializeA"]
old-location: dataxchg\ddeinitialize.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeinitialize.htm
ms.date: 12/05/2018
ms.keywords: APPCLASS_MONITOR, APPCLASS_STANDARD, APPCMD_CLIENTONLY, APPCMD_FILTERINITS, CBF_FAIL_ADVISES, CBF_FAIL_ALLSVRXACTIONS, CBF_FAIL_CONNECTIONS, CBF_FAIL_EXECUTES, CBF_FAIL_POKES, CBF_FAIL_REQUESTS, CBF_FAIL_SELFCONNECTIONS, CBF_SKIP_ALLNOTIFICATIONS, CBF_SKIP_CONNECT_CONFIRMS, CBF_SKIP_DISCONNECTS, CBF_SKIP_REGISTRATIONS, CBF_SKIP_UNREGISTRATIONS, DdeInitialize, DdeInitialize function [Data Exchange], DdeInitializeA, DdeInitializeW, MF_CALLBACKS, MF_CONV, MF_ERRORS, MF_HSZ_INFO, MF_LINKS, MF_POSTMSGS, MF_SENDMSGS, _win32_DdeInitialize, _win32_ddeinitialize_cpp, dataxchg.ddeinitialize, ddeml/DdeInitialize, ddeml/DdeInitializeA, ddeml/DdeInitializeW, winui._win32_ddeinitialize
req.header: ddeml.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DdeInitializeW (Unicode) and DdeInitializeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DdeInitializeA
 - ddeml/DdeInitializeA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - DdeInitialize
 - DdeInitializeA
 - DdeInitializeW
---

# DdeInitializeA function


## -description

Registers an application with the <a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a> (DDEML). An application must call this function before calling any other Dynamic Data Exchange Management Library (DDEML) function.

## -parameters

### -param pidInst [in, out]

Type: <b>LPDWORD</b>

The application instance identifier. At initialization, this parameter should point to 0. If the function succeeds, this parameter points to the instance identifier for the application. This value should be passed as the 
					<i>idInst</i> parameter in all other DDEML functions that require it. If an application uses multiple instances of the DDEML dynamic-link library (DLL), the application should provide a different callback function for each instance. 

If 
					<i>pidInst</i> points to a nonzero value, reinitialization of the DDEML is implied. In this case, 
					<i>pidInst</i> must point to a valid application-instance identifier.

### -param pfnCallback [in]

Type: <b>PFNCALLBACK</b>

A pointer to the application-defined DDE callback function. This function processes DDE transactions sent by the system. For more information, see the <a href="/windows/desktop/api/ddeml/nc-ddeml-pfncallback">DdeCallback</a> callback function.

### -param afCmd [in]

Type: <b>DWORD</b>

A set of <b>APPCMD_</b>, <b>CBF_</b>, and <b>MF_</b> flags. The <b>APPCMD_</b> flags provide special instructions to <b>DdeInitialize</b>. The <b>CBF_</b> flags specify filters that prevent specific types of transactions from reaching the callback function. The <b>MF_</b> flags specify the types of DDE activity that a DDE monitoring application monitors. Using these flags enhances the performance of a DDE application by eliminating unnecessary calls to the callback function. 

This parameter can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="APPCLASS_MONITOR"></a><a id="appclass_monitor"></a><dl>
<dt><b>APPCLASS_MONITOR</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
Makes it possible for the application to monitor DDE activity in the system. This flag is for use by DDE monitoring applications. The application specifies the types of DDE activity to monitor by combining one or more monitor flags with the <b>APPCLASS_MONITOR</b> flag. For details, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="APPCLASS_STANDARD"></a><a id="appclass_standard"></a><dl>
<dt><b>APPCLASS_STANDARD</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Registers the application as a standard (nonmonitoring) DDEML application.

</td>
</tr>
<tr>
<td width="40%"><a id="APPCMD_CLIENTONLY"></a><a id="appcmd_clientonly"></a><dl>
<dt><b>APPCMD_CLIENTONLY</b></dt>
<dt>0x00000010L</dt>
</dl>
</td>
<td width="60%">
Prevents the application from becoming a server in a DDE conversation. The application can only be a client. This flag reduces consumption of resources by the DDEML. It includes the functionality of the <b>CBF_FAIL_ALLSVRXACTIONS</b> flag.

</td>
</tr>
<tr>
<td width="40%"><a id="APPCMD_FILTERINITS"></a><a id="appcmd_filterinits"></a><dl>
<dt><b>APPCMD_FILTERINITS</b></dt>
<dt>0x00000020L</dt>
</dl>
</td>
<td width="60%">
Prevents the DDEML from sending <a href="/windows/desktop/dataxchg/xtyp-connect">XTYP_CONNECT</a> and <a href="/windows/desktop/dataxchg/xtyp-wildconnect">XTYP_WILDCONNECT</a> transactions to the application until the application has created its string handles and registered its service names or has turned off filtering by a subsequent call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddenameservice">DdeNameService</a> or <b>DdeInitialize</b> function. This flag is always in effect when an application calls <b>DdeInitialize</b> for the first time, regardless of whether the application specifies the flag. On subsequent calls to <b>DdeInitialize</b>, not specifying this flag turns off the application's service-name filters, but specifying it turns on the application's service name filters.

</td>
</tr>
<tr>
<td width="40%"><a id="CBF_FAIL_ALLSVRXACTIONS"></a><a id="cbf_fail_allsvrxactions"></a><dl>
<dt><b>CBF_FAIL_ALLSVRXACTIONS</b></dt>
<dt>0x0003f000</dt>
</dl>
</td>
<td width="60%">
Prevents the callback function from receiving server transactions. The system returns <b>DDE_FNOTPROCESSED</b> to each client that sends a transaction to this application. This flag is equivalent to combining all CBF_FAIL_ flags.

</td>
</tr>
<tr>
<td width="40%"><a id="CBF_FAIL_ADVISES"></a><a id="cbf_fail_advises"></a><dl>
<dt><b>CBF_FAIL_ADVISES</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
Prevents the callback function from receiving <a href="/windows/desktop/dataxchg/xtyp-advstart">XTYP_ADVSTART</a> and <a href="/windows/desktop/dataxchg/xtyp-advstop">XTYP_ADVSTOP</a> transactions. The system returns <b>DDE_FNOTPROCESSED</b> to each client that sends an <b>XTYP_ADVSTART</b> or <b>XTYP_ADVSTOP</b> transaction to the server.

</td>
</tr>
<tr>
<td width="40%"><a id="CBF_FAIL_CONNECTIONS"></a><a id="cbf_fail_connections"></a><dl>
<dt><b>CBF_FAIL_CONNECTIONS</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Prevents the callback function from receiving <a href="/windows/desktop/dataxchg/xtyp-connect">XTYP_CONNECT</a> and <a href="/windows/desktop/dataxchg/xtyp-wildconnect">XTYP_WILDCONNECT</a> transactions.

</td>
</tr>
<tr>
<td width="40%"><a id="CBF_FAIL_EXECUTES"></a><a id="cbf_fail_executes"></a><dl>
<dt><b>CBF_FAIL_EXECUTES</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Prevents the callback function from receiving <a href="/windows/desktop/dataxchg/xtyp-execute">XTYP_EXECUTE</a> transactions. The system returns <b>DDE_FNOTPROCESSED</b> to a client that sends an 
						<b>XTYP_EXECUTE</b> transaction to the server.

</td>
</tr>
<tr>
<td width="40%"><a id="CBF_FAIL_POKES"></a><a id="cbf_fail_pokes"></a><dl>
<dt><b>CBF_FAIL_POKES</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Prevents the callback function from receiving <a href="/windows/desktop/dataxchg/xtyp-poke">XTYP_POKE</a> transactions. The system returns <b>DDE_FNOTPROCESSED</b> to a client that sends an 
						<b>XTYP_POKE</b> transaction to the server.

</td>
</tr>
<tr>
<td width="40%"><a id="CBF_FAIL_REQUESTS"></a><a id="cbf_fail_requests"></a><dl>
<dt><b>CBF_FAIL_REQUESTS</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Prevents the callback function from receiving <a href="/windows/desktop/dataxchg/xtyp-request">XTYP_REQUEST</a> transactions. The system returns <b>DDE_FNOTPROCESSED</b> to a client that sends an 
						<b>XTYP_REQUEST</b> transaction to the server.

</td>
</tr>
<tr>
<td width="40%"><a id="CBF_FAIL_SELFCONNECTIONS"></a><a id="cbf_fail_selfconnections"></a><dl>
<dt><b>CBF_FAIL_SELFCONNECTIONS</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
Prevents the callback function from receiving <a href="/windows/desktop/dataxchg/xtyp-connect">XTYP_CONNECT</a> transactions from the application's own instance. This flag prevents an application from establishing a DDE conversation with its own instance. An application should use this flag if it needs to communicate with other instances of itself but not with itself.

</td>
</tr>
<tr>
<td width="40%"><a id="CBF_SKIP_ALLNOTIFICATIONS"></a><a id="cbf_skip_allnotifications"></a><dl>
<dt><b>CBF_SKIP_ALLNOTIFICATIONS</b></dt>
<dt>0x003c0000</dt>
</dl>
</td>
<td width="60%">
Prevents the callback function from receiving any notifications. This flag is equivalent to combining all CBF_SKIP_ flags.

</td>
</tr>
<tr>
<td width="40%"><a id="CBF_SKIP_CONNECT_CONFIRMS"></a><a id="cbf_skip_connect_confirms"></a><dl>
<dt><b>CBF_SKIP_CONNECT_CONFIRMS</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Prevents the callback function from receiving <a href="/windows/desktop/dataxchg/xtyp-connect-confirm">XTYP_CONNECT_CONFIRM</a> notifications.

</td>
</tr>
<tr>
<td width="40%"><a id="CBF_SKIP_DISCONNECTS"></a><a id="cbf_skip_disconnects"></a><dl>
<dt><b>CBF_SKIP_DISCONNECTS</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
Prevents the callback function from receiving <a href="/windows/desktop/dataxchg/xtyp-disconnect">XTYP_DISCONNECT</a> notifications.

</td>
</tr>
<tr>
<td width="40%"><a id="CBF_SKIP_REGISTRATIONS"></a><a id="cbf_skip_registrations"></a><dl>
<dt><b>CBF_SKIP_REGISTRATIONS</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
Prevents the callback function from receiving <a href="/windows/desktop/dataxchg/xtyp-register">XTYP_REGISTER</a> notifications.

</td>
</tr>
<tr>
<td width="40%"><a id="CBF_SKIP_UNREGISTRATIONS"></a><a id="cbf_skip_unregistrations"></a><dl>
<dt><b>CBF_SKIP_UNREGISTRATIONS</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
Prevents the callback function from receiving <a href="/windows/desktop/dataxchg/xtyp-unregister">XTYP_UNREGISTER</a> notifications.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_CALLBACKS"></a><a id="mf_callbacks"></a><dl>
<dt><b>MF_CALLBACKS</b></dt>
<dt>0x08000000</dt>
</dl>
</td>
<td width="60%">
Notifies the callback function whenever a transaction is sent to any DDE callback function in the system.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_CONV"></a><a id="mf_conv"></a><dl>
<dt><b>MF_CONV</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
Notifies the callback function whenever a conversation is established or terminated.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_ERRORS"></a><a id="mf_errors"></a><dl>
<dt><b>MF_ERRORS</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Notifies the callback function whenever a DDE error occurs.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_HSZ_INFO"></a><a id="mf_hsz_info"></a><dl>
<dt><b>MF_HSZ_INFO</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
Notifies the callback function whenever a DDE application creates, frees, or increments the usage count of a string handle or whenever a string handle is freed as a result of a call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeuninitialize">DdeUninitialize</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_LINKS"></a><a id="mf_links"></a><dl>
<dt><b>MF_LINKS</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Notifies the callback function whenever an advise loop is started or ended.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_POSTMSGS"></a><a id="mf_postmsgs"></a><dl>
<dt><b>MF_POSTMSGS</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
Notifies the callback function whenever the system or an application posts a DDE message.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_SENDMSGS"></a><a id="mf_sendmsgs"></a><dl>
<dt><b>MF_SENDMSGS</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
Notifies the callback function whenever the system or an application sends a DDE message.

</td>
</tr>
</table>

### -param ulRes

Type: <b>DWORD</b>

Reserved; must be set to zero.

## -returns

Type: <b>UINT</b>

If the function succeeds, the return value is <b>DMLERR_NO_ERROR</b>. 

If the function fails, the return value is one of the following values:

## -remarks

An application that uses multiple instances of the DDEML must not pass DDEML objects between instances. 

A DDE monitoring application should not attempt to perform DDE operations (establish conversations, issue transactions, and so on) within the context of the same application instance. 

A synchronous transaction fails with a <b>DMLERR_REENTRANCY</b> error if any instance of the same task has a synchronous transaction already in progress. 

The <b>CBF_FAIL_ALLSVRXACTIONS</b> flag causes the DDEML to filter all server transactions and can be changed by a subsequent call to <b>DdeInitialize</b>. The <b>APPCMD_CLIENTONLY</b> flag prevents the DDEML from creating key resources for the server and cannot be changed by a subsequent call to <b>DdeInitialize</b>. 

There is an ANSI version and a Unicode version of <b>DdeInitialize</b>. The version called determines the type of the window procedures used to control DDE conversations (ANSI or Unicode), and the default value for the 
				<i>iCodePage</i> member of the 
				<a href="/windows/desktop/api/ddeml/ns-ddeml-convcontext">CONVCONTEXT</a> structure (<b>CP_WINANSI</b> or <b>CP_WINUNICODE</b>). 





> [!NOTE]
> The ddeml.h header defines DdeInitialize as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library Overview</a>
