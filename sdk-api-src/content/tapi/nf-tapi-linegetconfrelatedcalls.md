---
UID: NF:tapi.lineGetConfRelatedCalls
title: lineGetConfRelatedCalls function
author: windows-sdk-content
description: The lineGetConfRelatedCalls function returns a list of call handles that are part of the same conference call as the specified call.
old-location: tapi2\linegetconfrelatedcalls.htm
tech.root: Tapi
ms.assetid: 048bc4bc-511a-4666-a2ff-4fff5132ed2e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "_tapi2_linegetconfrelatedcalls, lineGetConfRelatedCalls, lineGetConfRelatedCalls function [TAPI 2.2], tapi/lineGetConfRelatedCalls, tapi2.linegetconfrelatedcalls"
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
 - lineGetConfRelatedCalls
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- lineGetConfRelatedCalls
: 
---

# lineGetConfRelatedCalls function


## -description


The 
<b>lineGetConfRelatedCalls</b> function returns a list of call handles that are part of the same conference call as the specified call. The specified call is either a conference call or a participant call in a conference call. New handles are generated for those calls for which the application does not already have handles, and the application is granted monitor privilege to those calls.


## -parameters




### -param hCall

Handle to a call. This is either a conference call or a participant call in a conference call. For a conference parent call, the call state of <i>hCall</i> can be any state. For a conference participant call, it must be in the <i>conferenced</i> state.


### -param lpCallList

Pointer to a variably sized data structure of type 
<a href="https://msdn.microsoft.com/b715dd07-74bd-4267-91fe-cfc0cd1e6aa4">LINECALLLIST</a>. Upon successful completion of the request, call handles to all calls in the conference call are returned in this structure. The first call in the list is the conference call, the other calls are the participant calls. The application is granted monitor privilege to those calls for which it does not already have handles; the privileges to calls in the list for which the application already has handles is unchanged. Prior to calling 
<b>lineGetConfRelatedCalls</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="https://msdn.microsoft.com/61313fe3-74a1-4195-b5af-37463dad02c1">memory allocation</a> topic. </div>
<div> </div>

## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_NOCONFERENCE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_STRUCTURETOOSMALL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.




## -remarks



The specified call can either be a conference call handle or a handle to a participant call. For example, a consultation call that has not yet been added to a conference call is not part of a conference. The first entry in the list that is returned is the conference call handle, the other handles are all the participant calls. The specified call is always one of the calls returned in the list. Calls in the list to which the application does not already have a call handle are assigned monitor privilege; privileges to calls for which the application already has handles are unchanged. The application can use 
<a href="https://msdn.microsoft.com/a13d7cfd-3709-43fb-88b9-291928f2c0d8">lineSetCallPrivilege</a> to change the privilege of the call.

If 
<b>lineGetConfRelatedCalls</b> is called immediately after a call is added to a conference using 
<a href="https://msdn.microsoft.com/ebedf664-4c45-49c3-9d86-c3d782077a00">lineCompleteTransfer</a>, 
<b>lineGetConfRelatedCalls</b> may not return a complete list of related calls because TAPI waits to receive a 
<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a> message indicating that the call has entered LINECALLSTATE_CONFERENCED before it considers the call to actually be part of the conference (that is, the <i>conferenced</i> state is confirmed by the service provider). After the application has received the LINE_CALLSTATE message, 
<b>lineGetConfRelatedCalls</b> returns complete information.

The application can invoke 
<a href="https://msdn.microsoft.com/e69722cb-9c45-4f1a-a855-64afa3c33276">lineGetCallInfo</a> and 
<a href="https://msdn.microsoft.com/88bcd211-0993-4703-b43f-4e0b93e3eb7e">lineGetCallStatus</a> for each call in the list to determine the call's information and status, respectively.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/ebedf664-4c45-49c3-9d86-c3d782077a00">lineCompleteTransfer</a>



<a href="https://msdn.microsoft.com/e69722cb-9c45-4f1a-a855-64afa3c33276">lineGetCallInfo</a>



<a href="https://msdn.microsoft.com/88bcd211-0993-4703-b43f-4e0b93e3eb7e">lineGetCallStatus</a>



<a href="https://msdn.microsoft.com/a13d7cfd-3709-43fb-88b9-291928f2c0d8">lineSetCallPrivilege</a>
 

 

