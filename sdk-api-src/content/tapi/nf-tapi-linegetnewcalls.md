---
UID: NF:tapi.lineGetNewCalls
title: lineGetNewCalls function
author: windows-sdk-content
description: The lineGetNewCalls function returns call handles to calls on a specified line or address for which the application currently does not have handles. The application is granted monitor privilege to these calls.
old-location: tapi2\linegetnewcalls.htm
tech.root: tapi
ms.assetid: 179af1a1-078f-401c-8c15-12fc8ca06e3c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_tapi2_linegetnewcalls, lineGetNewCalls, lineGetNewCalls function [TAPI 2.2], tapi/lineGetNewCalls, tapi2.linegetnewcalls"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineGetNewCalls
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineGetNewCalls function


## -description


The 
<b>lineGetNewCalls</b> function returns call handles to calls on a specified line or address for which the application currently does not have handles. The application is granted monitor privilege to these calls.


## -parameters




### -param hLine

Handle to an open line device.


### -param dwAddressID

Address on the given open line device. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.


### -param dwSelect

Selection of calls that are requested. This parameter uses one and only one of the 
<a href="https://msdn.microsoft.com/f19a41bc-403a-4d4b-ab85-240a73514ebb">LINECALLSELECT_ Constants</a>.


### -param lpCallList

Pointer to a variably sized data structure of type 
<a href="https://msdn.microsoft.com/b715dd07-74bd-4267-91fe-cfc0cd1e6aa4">LINECALLLIST</a>. Upon successful completion of the request, call handles to all selected calls are returned in this structure. Prior to calling 
<b>lineGetNewCalls</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="https://msdn.microsoft.com/61313fe3-74a1-4195-b5af-37463dad02c1">memory allocation</a> topic. </div>
<div> </div>

## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESSID, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSELECT, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALLINEHANDLE, LINEERR_STRUCTURETOOSMALL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NOMEM.




## -remarks



An application can use 
<b>lineGetNewCalls</b> to obtain handles to calls for which it currently has no handles. The application can select the calls for which handles are to be returned by basing this selection on scope (calls on a specified line, or calls on a specified address). For example, an application can request call handles to all calls on a given address for which it currently has no handle. The application is always given monitor privilege to the new call handles. Also, when opening a line, an application uses this function to become aware of existing calls.

The application can invoke 
<a href="https://msdn.microsoft.com/e69722cb-9c45-4f1a-a855-64afa3c33276">lineGetCallInfo</a> and 
<a href="https://msdn.microsoft.com/88bcd211-0993-4703-b43f-4e0b93e3eb7e">lineGetCallStatus</a> for each call in the list to determine the call's information and status, respectively. It can use 
<a href="https://msdn.microsoft.com/a13d7cfd-3709-43fb-88b9-291928f2c0d8">lineSetCallPrivilege</a> to change its privilege to owner.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/b715dd07-74bd-4267-91fe-cfc0cd1e6aa4">LINECALLLIST</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/e69722cb-9c45-4f1a-a855-64afa3c33276">lineGetCallInfo</a>



<a href="https://msdn.microsoft.com/88bcd211-0993-4703-b43f-4e0b93e3eb7e">lineGetCallStatus</a>



<a href="https://msdn.microsoft.com/a13d7cfd-3709-43fb-88b9-291928f2c0d8">lineSetCallPrivilege</a>
 

 

