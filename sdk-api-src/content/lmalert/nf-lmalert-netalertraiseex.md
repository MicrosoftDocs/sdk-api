---
UID: NF:lmalert.NetAlertRaiseEx
title: NetAlertRaiseEx function (lmalert.h)
description: The NetAlertRaiseEx function notifies all registered clients when a particular event occurs. You can call this extended function to simplify the sending of an alert message because NetAlertRaiseEx does not require that you specify a STD_ALERT structure.
helpviewer_keywords: ["ALERT_ADMIN_EVENT","ALERT_ERRORLOG_EVENT","ALERT_MESSAGE_EVENT","ALERT_PRINT_EVENT","ALERT_USER_EVENT","NetAlertRaiseEx","NetAlertRaiseEx function [Network Management]","_win32_netalertraiseex","lmalert/NetAlertRaiseEx","netmgmt.netalertraiseex"]
old-location: netmgmt\netalertraiseex.htm
tech.root: NetMgmt
ms.assetid: 9762f0d6-0022-4e05-b2d8-6223d7bbb2c8
ms.date: 12/05/2018
ms.keywords: ALERT_ADMIN_EVENT, ALERT_ERRORLOG_EVENT, ALERT_MESSAGE_EVENT, ALERT_PRINT_EVENT, ALERT_USER_EVENT, NetAlertRaiseEx, NetAlertRaiseEx function [Network Management], _win32_netalertraiseex, lmalert/NetAlertRaiseEx, netmgmt.netalertraiseex
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
 - NetAlertRaiseEx
 - lmalert/NetAlertRaiseEx
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
 - NetAlertRaiseEx
---

# NetAlertRaiseEx function


## -description

<p class="CCE_Message">[This function is not supported as of Windows Vista because the alerter service is not supported.]

The
				<b>NetAlertRaiseEx</b> function notifies all registered clients when a particular event occurs. You can call this extended function to simplify the sending of an alert message because 
<b>NetAlertRaiseEx</b> does not require that you specify a 
<a href="/windows/desktop/api/lmalert/ns-lmalert-std_alert">STD_ALERT</a> structure.

## -parameters

### -param AlertType [in]

A pointer to a constant string that specifies the alert class (type of alert) to raise. This parameter can be one of the following predefined values, or a user-defined alert class for network applications. (The event name for an alert can be any text string.) 



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

### -param VariableInfo [in]

A pointer to the data to send to the clients listening for the interrupting message. The data should consist of one 
<a href="/windows/desktop/api/lmalert/ns-lmalert-admin_other_info">ADMIN_OTHER_INFO</a>, 
<a href="/windows/desktop/api/lmalert/ns-lmalert-errlog_other_info">ERRLOG_OTHER_INFO</a>, 
<a href="/windows/desktop/api/lmalert/ns-lmalert-print_other_info">PRINT_OTHER_INFO</a>, or 
<a href="/windows/desktop/api/lmalert/ns-lmalert-user_other_info">USER_OTHER_INFO</a> structure followed by any required variable-length information. For more information, see the code sample in the following Remarks section. 




The calling application must allocate and free the memory for all structures and variable data. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

### -param VariableInfoSize [in]

The number of bytes of variable information in the buffer pointed to by the <i>VariableInfo</i> parameter.

### -param ServiceName [in]

A pointer to a constant string that specifies the name of the service raising the interrupting message.

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
A parameter is incorrect. This error is returned if the <i>AlertEventName</i>  parameter is <b>NULL</b> or an empty string, the <i>ServiceName</i>  parameter is <b>NULL</b> or an empty string, the <i>VariableInfo</i>  parameter is <b>NULL</b>, or the <i>VariableInfoSize</i>  parameter is greater than 512 minus the size of the <a href="/windows/desktop/api/lmalert/ns-lmalert-std_alert">STD_ALERT</a> structure. 

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
<b>NetAlertRaiseEx</b> function.

The alerter service must be running on the client computer when you call the 
<b>NetAlertRaiseEx</b> function, or the function fails with ERROR_FILE_NOT_FOUND.


#### Examples

The following code sample demonstrates how to raise the following types of interrupting messages (alerts) by calling the <b>NetAlertRaiseEx</b> function:

<ul>
<li>An administrative alert by specifying an <a href="/windows/desktop/api/lmalert/ns-lmalert-admin_other_info">ADMIN_OTHER_INFO</a> structure</li>
<li>A print alert by specifying a <a href="/windows/desktop/api/lmalert/ns-lmalert-print_other_info">PRINT_OTHER_INFO</a> structure</li>
<li>A user alert by specifying a <a href="/windows/desktop/api/lmalert/ns-lmalert-user_other_info">USER_OTHER_INFO</a> structure</li>
</ul>
In each instance the code assigns values to the members of the relevant alert information structure. Following this, the sample retrieves a pointer to the portion of the message buffer that follows the structure by calling the <a href="/windows/desktop/api/lmalert/nf-lmalert-alert_var_data">ALERT_VAR_DATA</a> macro. The code also fills in the variable-length strings in this portion of the buffer. Finally, the sample calls <b>NetAlertRaiseEx</b> to send the alert.

Note that the calling application must allocate and free the memory for all structures and variable-length data in an alert message buffer.

To pass a user-defined structure and valid strings in a user alert, you must create an event message file and link it with your application. You must also register the application in the <b>EventMessageFile</b> subkey in the <b>EventLog</b> section of the registry. If you do not register the application, the user alert will contain the information you pass in the variable-length strings that follow the <a href="/windows/desktop/api/lmalert/ns-lmalert-user_other_info">USER_OTHER_INFO</a> structure. For more information about <b>EventMessageFile</b>, see <a href="/windows/desktop/EventLog/event-logging">Event Logging</a>.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#pragma comment(lib, "netapi32.lib")

#include <windows.h>
#include <lm.h>
#include <stdio.h>
#include <time.h>
//
// Define default strings.
//
#define PROGRAM_NAME    TEXT("NETALRT")
#define szComputerName  TEXT("\\\\TESTCOMPUTER")
#define szUserName      TEXT("TEST")
#define szQueueName     TEXT("PQUEUE")
#define szDestName      TEXT("MYPRINTER")
#define szStatus        TEXT("OK")
//
// Define structure sizes.
//
#define VAREDSIZE 312  // maximum size of the variable length message
char buff[VAREDSIZE];
//
int main()
{
   time_t             now;
   PADMIN_OTHER_INFO  pAdminInfo; // ADMIN_OTHER_INFO structure
   PPRINT_OTHER_INFO  pPrintInfo; // PRINT_OTHER_INFO structure
   PUSER_OTHER_INFO   pUserInfo;  // USER_OTHER_INFO structure
   TCHAR              *p;
   DWORD dwResult; 

   time( &now );  // Retrieve the current time to print it later.

   //
   // Sending an administrative alert 
   //
   // Assign values to the members of the ADMIN_OTHER_INFO structure.
   //
   pAdminInfo = (PADMIN_OTHER_INFO) buff; 
   ZeroMemory(pAdminInfo, VAREDSIZE);
   //
   // Error 2377, NERR_LogOverflow, indicates
   //  a log file is full.
   //
   pAdminInfo->alrtad_errcode = 2377;
   pAdminInfo->alrtad_numstrings = 1;
   //
   // Retrieve a pointer to the variable data portion at the 
   //  end of the buffer by calling the ALERT_VAR_DATA macro.
   //
   p = (LPTSTR) ALERT_VAR_DATA(pAdminInfo); 
   //
   // Fill in the variable-length, concatenated strings 
   //  that follow the ADMIN_OTHER_INFO structure. These strings
   //  will be written to the message log.
   //
   wcscpy_s(p,VAREDSIZE/2, TEXT("'C:\\MYLOG.TXT'")); 
   //
   // Call the NetAlertRaiseEx function to raise the
   //  administrative alert.
   //
   dwResult = NetAlertRaiseEx(ALERT_ADMIN_EVENT, pAdminInfo, 255 , TEXT("MYSERVICE"));
   //
   // Display the results of the function call.
   //
   if (dwResult != NERR_Success)
   {
      wprintf(L"NetAlertRaiseEx failed: %d\n", dwResult);
      return -1;
   }
   else
      wprintf(L"Administrative alert raised successfully.\n");


   //
   // Sending a print alert
   //
   // Assign values to the members of the PRINT_OTHER_INFO structure.
   //
   pPrintInfo = (PPRINT_OTHER_INFO) buff; 
   ZeroMemory(pPrintInfo, VAREDSIZE);        
   pPrintInfo->alrtpr_jobid = 5457;
   pPrintInfo->alrtpr_status = 0;
   pPrintInfo->alrtpr_submitted = (DWORD) now;
   pPrintInfo->alrtpr_size = 1000;
   //
   // Retrieve a pointer to the variable data portion at the 
   //  end of the buffer by calling the ALERT_VAR_DATA macro. 
   //
   p = (LPTSTR) ALERT_VAR_DATA(pPrintInfo);  
   //
   // Fill in the variable-length, concatenated strings 
   //  that follow the PRINT_OTHER_INFO structure. 
   //
   wcscpy_s(p, VAREDSIZE/2, szComputerName); // computername 
   p += lstrlen(p) + 1;
   wcscpy_s(p, (VAREDSIZE/2)-wcslen(szComputerName)-1, szUserName);     // user name
   p += lstrlen(p) + 1;
   wcscpy_s(p, (VAREDSIZE/2)-wcslen(szComputerName)-wcslen(szUserName)-2, 
       szQueueName);    // printer queuename
   p += lstrlen(p) + 1;
   wcscpy_s(p, (VAREDSIZE/2)-wcslen(szComputerName)-wcslen(szUserName)-wcslen(szQueueName)-3,
       szDestName);     // destination or printer name (optional)
   p += lstrlen(p) + 1;
   wcscpy_s(p, (VAREDSIZE/2)-wcslen(szComputerName)-wcslen(szUserName)-wcslen(szQueueName) 
       - wcslen(szDestName)-4, szStatus);       // status of the print job (optional)
   //
   // Call the NetAlertRaiseEx function to raise the
   //  print alert.
   //
   dwResult = NetAlertRaiseEx(ALERT_PRINT_EVENT, pPrintInfo, VAREDSIZE, TEXT("MYSERVICE"));
   //
   // Display the results of the function call.
   //
   if (dwResult != NERR_Success)
   {
      wprintf(L"NetAlertRaiseEx failed: %d\n", dwResult);
      return -1;
   }
   else
      wprintf(L"Print alert raised successfully.\n");


   //
   // Sending a user alert
   //
   // Assign values to the members of the USER_OTHER_INFO structure.
   //
   pUserInfo  = (PUSER_OTHER_INFO)  buff; 
   ZeroMemory(pUserInfo, VAREDSIZE);
   pUserInfo->alrtus_errcode = 0xffff;
   pUserInfo->alrtus_numstrings = 1;
   //
   // Retrieve a pointer to the variable data portion at the 
   //  end of the buffer by calling the ALERT_VAR_DATA macro.
   //
   p = (LPTSTR) ALERT_VAR_DATA(pUserInfo); 
   //
   // Fill in the variable-length, concatenated strings 
   //  that follow the USER_OTHER_INFO structure.
   //
   wcscpy_s(p,(VAREDSIZE/2), TEXT("C:\\USERLOG.TXT"));
   p += lstrlen(p) + 1;
   wcscpy_s(p, (VAREDSIZE/2) - wcslen(TEXT("C:\\USERLOG.TXT"))-1, szUserName);
   //
   // Call the NetAlertRaiseEx function to raise the
   //  user alert.
   //
   dwResult = NetAlertRaiseEx(ALERT_USER_EVENT, pUserInfo, VAREDSIZE, TEXT("MYSERVICE"));
   //
   // Display the results of the function call.
   //
   if (dwResult != NERR_Success)
   {
      wprintf(L"NetAlertRaiseEx failed: %d\n", dwResult);
      return -1;
   }
   else
      wprintf(L"User alert raised successfully.\n");

   return(dwResult);   
}

```

## -see-also

<a href="/windows/desktop/api/lmalert/ns-lmalert-admin_other_info">ADMIN_OTHER_INFO</a>



<a href="/windows/desktop/api/lmalert/nf-lmalert-alert_var_data">ALERT_VAR_DATA</a>



<a href="/windows/desktop/NetMgmt/alert-functions">Alert Functions</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-errlog_other_info">ERRLOG_OTHER_INFO</a>



<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraise">NetAlertRaise</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-print_other_info">PRINT_OTHER_INFO</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-user_other_info">USER_OTHER_INFO</a>