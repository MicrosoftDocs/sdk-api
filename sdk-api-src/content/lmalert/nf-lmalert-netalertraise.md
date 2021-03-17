---
UID: NF:lmalert.NetAlertRaise
title: NetAlertRaise function (lmalert.h)
description: The NetAlertRaise function notifies all registered clients when a particular event occurs.
helpviewer_keywords: ["ALERT_ADMIN_EVENT","ALERT_ERRORLOG_EVENT","ALERT_MESSAGE_EVENT","ALERT_PRINT_EVENT","ALERT_USER_EVENT","NetAlertRaise","NetAlertRaise function [Network Management]","_win32_netalertraise","lmalert/NetAlertRaise","netmgmt.netalertraise"]
old-location: netmgmt\netalertraise.htm
tech.root: NetMgmt
ms.assetid: 11367a72-c21d-4044-98cf-a7a30cc43a8b
ms.date: 12/05/2018
ms.keywords: ALERT_ADMIN_EVENT, ALERT_ERRORLOG_EVENT, ALERT_MESSAGE_EVENT, ALERT_PRINT_EVENT, ALERT_USER_EVENT, NetAlertRaise, NetAlertRaise function [Network Management], _win32_netalertraise, lmalert/NetAlertRaise, netmgmt.netalertraise
req.header: lmalert.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetAlertRaise
 - lmalert/NetAlertRaise
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetAlertRaise
---

# NetAlertRaise function


## -description

<p class="CCE_Message">[This function is not supported as of Windows Vista because the alerter service is not supported.]

The
				<b>NetAlertRaise</b> function notifies all registered clients when a particular event occurs.

To simplify sending an alert message, you can call the extended function 
<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraiseex">NetAlertRaiseEx</a> instead. 
<b>NetAlertRaiseEx</b> does not require that you specify a 
<a href="/windows/desktop/api/lmalert/ns-lmalert-std_alert">STD_ALERT</a> structure.

## -parameters

### -param AlertType [in]

A pointer to a constant string that specifies the alert class (type of alert) to raise. This parameter can be one of the following predefined values, or a user-defined alert class for network applications. The event name for an alert can be any text string. 



<table>
<tr>
<th>Name</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ALERT_ADMIN_EVENT"></a><a id="alert_admin_event"></a><dl>
<dt><b>ALERT_ADMIN_EVENT</b></dt>
</dl>
</td>
<td width="60%">
An administrator's intervention is required.

</td>
</tr>
<tr>
<td width="40%"><a id="ALERT_ERRORLOG_EVENT"></a><a id="alert_errorlog_event"></a><dl>
<dt><b>ALERT_ERRORLOG_EVENT</b></dt>
</dl>
</td>
<td width="60%">
An entry was added to the error log.

</td>
</tr>
<tr>
<td width="40%"><a id="ALERT_MESSAGE_EVENT"></a><a id="alert_message_event"></a><dl>
<dt><b>ALERT_MESSAGE_EVENT</b></dt>
</dl>
</td>
<td width="60%">
A user or application received a broadcast message.

</td>
</tr>
<tr>
<td width="40%"><a id="ALERT_PRINT_EVENT"></a><a id="alert_print_event"></a><dl>
<dt><b>ALERT_PRINT_EVENT</b></dt>
</dl>
</td>
<td width="60%">
A print job completed or a print error occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="ALERT_USER_EVENT"></a><a id="alert_user_event"></a><dl>
<dt><b>ALERT_USER_EVENT</b></dt>
</dl>
</td>
<td width="60%">
An application or resource was used.

</td>
</tr>
</table>

### -param Buffer [in]

A pointer to the data to send to the clients listening for the interrupting message. The data should begin with a fixed-length 
<a href="/windows/desktop/api/lmalert/ns-lmalert-std_alert">STD_ALERT</a> structure followed by additional message data in one 
<a href="/windows/desktop/api/lmalert/ns-lmalert-admin_other_info">ADMIN_OTHER_INFO</a>, 
<a href="/windows/desktop/api/lmalert/ns-lmalert-errlog_other_info">ERRLOG_OTHER_INFO</a>, 
<a href="/windows/desktop/api/lmalert/ns-lmalert-print_other_info">PRINT_OTHER_INFO</a>, or 
<a href="/windows/desktop/api/lmalert/ns-lmalert-user_other_info">USER_OTHER_INFO</a> structure. Finally, the buffer should include any required variable-length information. For more information, see the code sample in the following Remarks section. 




The calling application must allocate and free the memory for all structures and variable data. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

### -param BufferSize [in]

The size, in bytes, of the message buffer.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code and a can be one of the following error codes. For a list of all possible error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if the <i>AlertEventName</i>  parameter is <b>NULL</b> or an empty string, the <i>Buffer</i>  parameter is <b>NULL</b>, or the <i>BufferSize</i>  parameter is less than the size of the <a href="/windows/desktop/api/lmalert/ns-lmalert-std_alert">STD_ALERT</a> structure plus the fixed size for the additional message data structure. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned on Windows Vista and later since the Alerter service is not supported.

</td>
</tr>
</table>

## -remarks

No special group membership is required to successfully execute the 
<b>NetAlertRaise</b> function.

The alerter service must be running on the client computer when you call the 
<b>NetAlertRaise</b> function, or the function fails with ERROR_FILE_NOT_FOUND.


#### Examples

The following code sample demonstrates how to raise an administrative alert by calling the 
<b>NetAlertRaise</b> function and specifying 
<a href="/windows/desktop/api/lmalert/ns-lmalert-std_alert">STD_ALERT</a> and 
<a href="/windows/desktop/api/lmalert/ns-lmalert-admin_other_info">ADMIN_OTHER_INFO</a> structures. First, the sample calculates the size of the message buffer. Then it allocates the buffer with a call to the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> function. The code assigns values to the members of the 
<b>STD_ALERT</b> and the 
<b>ADMIN_OTHER_INFO</b> portions of the buffer. The sample retrieves a pointer to the 
<b>ADMIN_OTHER_INFO</b> structure by calling the 
<a href="/windows/desktop/api/lmalert/nf-lmalert-alert_other_info">ALERT_OTHER_INFO</a> macro. It also retrieves a pointer to the variable data portion of the buffer by calling the 
<a href="/windows/desktop/api/lmalert/nf-lmalert-alert_var_data">ALERT_VAR_DATA</a> macro. Finally, the code sample frees the memory allocated for the buffer with a call to the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalfree">GlobalFree</a> function.


```cpp
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "netapi32.lib")

#include <windows.h>
#include <stdio.h>
#include <time.h>
#include <lm.h>

const int ALERT_VAR_DATA_SIZE = 216;

int wmain(int argc, wchar_t *argv[])
{
   int nBufferSize;
   LPVOID pAlertOtherInfo;
   PSTD_ALERT pStdAlert;              // STD_ALERT structure
   PADMIN_OTHER_INFO pAdminOtherInfo; // ADMIN_OTHER_INFO structure
   LPVOID pVarData; 
   time_t now;
   DWORD dwResult;
   //
   // Check command line arguments.
   //
   if (argc != 2)
   {
      fwprintf(stderr, L"Usage: %s LogFileName\n", argv[0]);
      exit(1);
   }
   // Calculate the buffer size;
   //  then allocate the memory for the buffer.
   //
   nBufferSize  = sizeof(STD_ALERT) + ALERT_VAR_DATA_SIZE;
   pAlertOtherInfo = (LPVOID) GlobalAlloc(GPTR, nBufferSize);

   if (pAlertOtherInfo == NULL)
   {
       fwprintf(stderr, L"Unable to allocate memory\n");
       exit(1);
   }

   //
   // Assign values to the STD_ALERT portion of the buffer.
   //   (This is required when you call NetAlertRaise.)
   //
   pStdAlert = (PSTD_ALERT)pAlertOtherInfo;
   time( &now );
   pStdAlert->alrt_timestamp = (DWORD)now;
   wcscpy_s(pStdAlert->alrt_eventname, EVLEN + 1, ALERT_ADMIN_EVENT);
   wcscpy_s(pStdAlert->alrt_servicename, SNLEN + 1, argv[0]);
   //
   // Retrieve the pointer to the ADMIN_OTHER_INFO structure 
   //  that follows the STD_ALERT portion of the buffer.
   //   Do this by calling the ALERT_OTHER_INFO macro.
   //
   pAdminOtherInfo = (PADMIN_OTHER_INFO)ALERT_OTHER_INFO(pAlertOtherInfo);
   //
   // Assign values to the ADMIN_OTHER_INFO structure.
   //
   pAdminOtherInfo->alrtad_numstrings = 1;
   //
   // Error 2377, NERR_LogOverflow, indicates
   //  a log file is full.
   //
   pAdminOtherInfo->alrtad_errcode = 2377;
   //
   // Retrieve the pointer to the variable data portion
   //  of the buffer by calling the ALERT_VAR_DATA macro.
   //
   pVarData = (LPTSTR)ALERT_VAR_DATA(pAdminOtherInfo);
   //
   // Supply the log file name for error 2377.
   //
   wcsncpy_s((wchar_t*) pVarData, ALERT_VAR_DATA_SIZE/2, 
           argv[1],
           ALERT_VAR_DATA_SIZE/2 );
   //
   // Send an administrative alert by calling the
   //  NetAlertRaise function.
   //
   dwResult = NetAlertRaise(ALERT_ADMIN_EVENT,
                            pAlertOtherInfo,
                            nBufferSize);
   //
   // Display the results of the function call.
   //
   if (dwResult != NERR_Success)
      wprintf(L"NetAlertRaise failed: %d\n", dwResult);
   else
      wprintf(L"Administrative alert raised successfully.\n");
   //
   // Free the allocated memory.
   //
   GlobalFree(pAlertOtherInfo);

   return (dwResult);
}

```

## -see-also

<a href="/windows/desktop/api/lmalert/ns-lmalert-admin_other_info">ADMIN_OTHER_INFO</a>



<a href="/windows/desktop/api/lmalert/nf-lmalert-alert_other_info">ALERT_OTHER_INFO</a>



<a href="/windows/desktop/api/lmalert/nf-lmalert-alert_var_data">ALERT_VAR_DATA</a>



<a href="/windows/desktop/NetMgmt/alert-functions">Alert Functions</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-errlog_other_info">ERRLOG_OTHER_INFO</a>



<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraiseex">NetAlertRaiseEx</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-print_other_info">PRINT_OTHER_INFO</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-std_alert">STD_ALERT</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-user_other_info">USER_OTHER_INFO</a>