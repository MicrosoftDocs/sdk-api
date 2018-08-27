---
UID: NF:lmalert.NetAlertRaise
title: NetAlertRaise function
author: windows-sdk-content
description: The NetAlertRaise function notifies all registered clients when a particular event occurs.
old-location: netmgmt\netalertraise.htm
old-project: netmgmt
ms.assetid: 11367a72-c21d-4044-98cf-a7a30cc43a8b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ALERT_ADMIN_EVENT, ALERT_ERRORLOG_EVENT, ALERT_MESSAGE_EVENT, ALERT_PRINT_EVENT, ALERT_USER_EVENT, NetAlertRaise, NetAlertRaise function [Network Management], _win32_netalertraise, lmalert/NetAlertRaise, netmgmt.netalertraise
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lmalert.h
req.include-header: Lm.h
req.redist: 
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
tech.root: 
req.typenames: USER_MODALS_INFO_3, *PUSER_MODALS_INFO_3, *LPUSER_MODALS_INFO_3
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetAlertRaise
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetAlertRaise function


## -description


<p class="CCE_Message">[This function is not supported as of Windows Vista because the alerter service is not supported.]

The
				<b>NetAlertRaise</b> function notifies all registered clients when a particular event occurs.

To simplify sending an alert message, you can call the extended function 
<a href="https://msdn.microsoft.com/9762f0d6-0022-4e05-b2d8-6223d7bbb2c8">NetAlertRaiseEx</a> instead. 
<b>NetAlertRaiseEx</b> does not require that you specify a 
<a href="https://msdn.microsoft.com/daa4594f-e59e-4f05-8183-677bee4ea446">STD_ALERT</a> structure.


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
<a href="https://msdn.microsoft.com/daa4594f-e59e-4f05-8183-677bee4ea446">STD_ALERT</a> structure followed by additional message data in one 
<a href="https://msdn.microsoft.com/43119dcf-7d04-4e3b-b1dc-20e814fbdc2f">ADMIN_OTHER_INFO</a>, 
<a href="https://msdn.microsoft.com/832ebe88-e1c4-4ce3-8057-922419b577f7">ERRLOG_OTHER_INFO</a>, 
<a href="https://msdn.microsoft.com/f2fd87bc-abde-43c0-b29d-d43cc5f038b8">PRINT_OTHER_INFO</a>, or 
<a href="https://msdn.microsoft.com/2f6bd906-fdab-410a-8856-4482e047371f">USER_OTHER_INFO</a> structure. Finally, the buffer should include any required variable-length information. For more information, see the code sample in the following Remarks section. 




The calling application must allocate and free the memory for all structures and variable data. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>.


### -param BufferSize [in]

The size, in bytes, of the message buffer.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code and a can be one of the following error codes. For a list of all possible error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.

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
A parameter is incorrect. This error is returned if the <i>AlertEventName</i>  parameter is <b>NULL</b> or an empty string, the <i>Buffer</i>  parameter is <b>NULL</b>, or the <i>BufferSize</i>  parameter is less than the size of the <a href="https://msdn.microsoft.com/daa4594f-e59e-4f05-8183-677bee4ea446">STD_ALERT</a> structure plus the fixed size for the additional message data structure. 

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
<a href="https://msdn.microsoft.com/daa4594f-e59e-4f05-8183-677bee4ea446">STD_ALERT</a> and 
<a href="https://msdn.microsoft.com/43119dcf-7d04-4e3b-b1dc-20e814fbdc2f">ADMIN_OTHER_INFO</a> structures. First, the sample calculates the size of the message buffer. Then it allocates the buffer with a call to the 
<a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a> function. The code assigns values to the members of the 
<b>STD_ALERT</b> and the 
<b>ADMIN_OTHER_INFO</b> portions of the buffer. The sample retrieves a pointer to the 
<b>ADMIN_OTHER_INFO</b> structure by calling the 
<a href="https://msdn.microsoft.com/e7bcc306-4b44-4230-96aa-a4717bb1fb11">ALERT_OTHER_INFO</a> macro. It also retrieves a pointer to the variable data portion of the buffer by calling the 
<a href="https://msdn.microsoft.com/ff71fb3d-8c01-47ac-93f2-108b1f49e2da">ALERT_VAR_DATA</a> macro. Finally, the code sample frees the memory allocated for the buffer with a call to the 
<a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a> function.


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




<a href="https://msdn.microsoft.com/43119dcf-7d04-4e3b-b1dc-20e814fbdc2f">ADMIN_OTHER_INFO</a>



<a href="https://msdn.microsoft.com/e7bcc306-4b44-4230-96aa-a4717bb1fb11">ALERT_OTHER_INFO</a>



<a href="https://msdn.microsoft.com/ff71fb3d-8c01-47ac-93f2-108b1f49e2da">ALERT_VAR_DATA</a>



<a href="https://msdn.microsoft.com/e131191b-7413-45ff-84cd-b3a873d33ca1">Alert Functions</a>



<a href="https://msdn.microsoft.com/832ebe88-e1c4-4ce3-8057-922419b577f7">ERRLOG_OTHER_INFO</a>



<a href="https://msdn.microsoft.com/9762f0d6-0022-4e05-b2d8-6223d7bbb2c8">NetAlertRaiseEx</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/f2fd87bc-abde-43c0-b29d-d43cc5f038b8">PRINT_OTHER_INFO</a>



<a href="https://msdn.microsoft.com/daa4594f-e59e-4f05-8183-677bee4ea446">STD_ALERT</a>



<a href="https://msdn.microsoft.com/2f6bd906-fdab-410a-8856-4482e047371f">USER_OTHER_INFO</a>
 

 

