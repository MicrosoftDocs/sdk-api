---
UID: NF:tapi.lineHandoffW
title: lineHandoffW function
author: windows-sdk-content
description: The lineHandoff function gives ownership of the specified call to another application. The application can be either specified directly by its file name or indirectly as the highest priority application that handles calls of the specified media mode.
old-location: tapi2\linehandoff.htm
tech.root: tapi
ms.assetid: 931c2fa4-dad6-432d-8f07-bb04b646916b
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "_tapi2_linehandoff, lineHandoff, lineHandoff function [TAPI 2.2], lineHandoffA, lineHandoffW, tapi/lineHandoff, tapi/lineHandoffA, tapi/lineHandoffW, tapi2.linehandoff"
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
req.unicode-ansi: lineHandoffW (Unicode) and lineHandoffA (ANSI)
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
 - lineHandoff
 - lineHandoffA
 - lineHandoffW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- lineHandoffW
: 
---

# lineHandoffW function


## -description


The 
<b>lineHandoff</b> function gives ownership of the specified call to another application. The application can be either specified directly by its file name or indirectly as the highest priority application that handles calls of the specified media mode.


## -parameters




### -param hCall

Handle to the call to be handed off. The application must be an owner of the call. The call state of <i>hCall</i> can be any state.


### -param lpszFileName

Pointer to a <b>null</b>-terminated string. If this pointer parameter is non-<b>NULL</b>, it contains the file name of the application that is the target of the handoff. If <b>NULL</b>, the handoff target is the highest priority application that has opened the line for owner privilege for the specified media mode. A valid file name does not include the path of the file.


### -param dwMediaMode

Media mode used to identify the target for the indirect handoff. The <i>dwMediaMode</i> parameter indirectly identifies the target application that is to receive ownership of the call. This parameter is ignored if <i>lpszFileName</i> is not <b>NULL</b>. This parameter uses one and only one of the 
<a href="https://msdn.microsoft.com/cbb758be-3ecd-4ac4-b1b5-57136a1aad8e">LINEMEDIAMODE_ Constants</a>.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALMEDIAMODE, LINEERR_TARGETNOTFOUND, LINEERR_INVALPOINTER, LINEERR_TARGETSELF, LINEERR_NOMEM, LINEERR_UNINITIALIZED, LINEERR_NOTOWNER.




## -remarks



The 
<b>lineHandoff</b> function returns LINEERR_TARGETSELF if the calling application attempted an indirect handoff (that is, set the <i>lpszFileName</i> parameter to <b>NULL</b>) and TAPI determined that the application is itself the highest priority application for the given media mode. If LINEERR_TARGETNOTFOUND is returned, a target for the call handoff was not found. This can occur if the named application did not open the same line with the LINECALLPRIVILEGE_OWNER bit in the <i>dwPrivileges</i> parameter of 
<a href="https://msdn.microsoft.com/7dd39866-0b3e-47be-8aa8-adfb66df6644">lineOpen</a>. Or, in the case of media-mode handoff, no application has opened the same line with the LINECALLPRIVILEGE_OWNER bit in the <i>dwPrivileges</i> parameter of 
<b>lineOpen</b> and with the media mode specified in the <i>dwMediaModes</i> parameter of 
<b>lineOpen</b>.

Call handoff allows ownership of a call to be passed among applications. There are two types of handoff. In the first type, if the application knows the file name of the target application, it can simply specify that file name. If an instance of the target application has opened the line device, ownership of the call is passed to the other application; otherwise, the handoff fails and an error is returned. This form of handoff succeeds if the call handle is handed off to the same file name as the application requesting the handoff.

The second type of handoff is based on media mode. In this case, the application indirectly specifies the target application by means of a media mode. The highest priority application that has currently opened the line device for that media mode is the target for the handoff. If there is no such application, the handoff fails and an error is returned.

The 
<b>lineHandoff</b> function does not change the media mode of a call. To change the media mode of a call, the application should use 
<a href="https://msdn.microsoft.com/4a0e3fd7-9483-4d21-9b6f-bb6c04aa8226">lineSetMediaMode</a> on the call, specifying the new media mode. This changes the call's media mode as stored in the call's 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> structure.

If handoff succeeds, the receiving application receives a 
<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a> message for the call. This message indicates that the receiving application has owner privilege to the call (<i>dwParam3</i>). In addition, the number of owners and/or monitors for the call may have changed. This is reported by the 
<a href="https://msdn.microsoft.com/eb882409-6842-434e-9f93-61cf0c11d1d0">LINE_CALLINFO</a> message, and the receiving application can then invoke 
<a href="https://msdn.microsoft.com/88bcd211-0993-4703-b43f-4e0b93e3eb7e">lineGetCallStatus</a> and 
<a href="https://msdn.microsoft.com/e69722cb-9c45-4f1a-a855-64afa3c33276">lineGetCallInfo</a> to retrieve more information about the received call.

The receiving application should first check the media mode in 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>. If only a single media mode flag is set, the call is officially of that media mode, and the application can act accordingly. If UNKNOWN and other media mode flags are set, then the media mode of the call is officially UNKNOWN but is assumed to be of one of the media modes for which a flag is set in 
<b>LINECALLINFO</b>. The application should assume that it ought to probe for the highest priority media mode.

If the probe succeeds (either for that media mode or for another one), the application should set the media mode member in 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> to the single media mode that was recognized. If the media mode flag matches the 
<b>LINECALLINFO</b> media mode, the application can act accordingly. If it makes a determination for another media mode, it must first hand off the call to that media mode.

If the probe fails, the application should clear the corresponding media mode flag in 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> and hand off the call, specifying <i>dwMediaMode</i> as LINEMEDIAMODE_UNKNOWN. It should also deallocate its call handle (or revert back to monitoring).

If none of the media modes succeeded in making a determination, only the UNKNOWN flag remains set in the media mode field of 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> at the time the media application attempts to hand off the call to UNKNOWN. The final 
<b>lineHandoff</b> fails if the application is the only remaining owner of the call. This informs the application that it should drop the call and deallocate its handle, in which case the call is abandoned. The privileges of the invoking application to the call are unchanged by this operation, but the application can change its privileges to a call with 
<a href="https://msdn.microsoft.com/a13d7cfd-3709-43fb-88b9-291928f2c0d8">lineSetCallPrivilege</a>.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/d6d188c9-9cbd-45af-93f0-b78850374919">Handoffs Overview</a>



<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/88bcd211-0993-4703-b43f-4e0b93e3eb7e">lineGetCallStatus</a>



<a href="https://msdn.microsoft.com/7dd39866-0b3e-47be-8aa8-adfb66df6644">lineOpen</a>



<a href="https://msdn.microsoft.com/a13d7cfd-3709-43fb-88b9-291928f2c0d8">lineSetCallPrivilege</a>



<a href="https://msdn.microsoft.com/4a0e3fd7-9483-4d21-9b6f-bb6c04aa8226">lineSetMediaMode</a>
 

 

