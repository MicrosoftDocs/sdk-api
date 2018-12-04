---
UID: NF:tapi.lineGetAppPriority
title: lineGetAppPriority function
author: windows-sdk-content
description: Enables an application to determine whether or not it is in the handoff priority list for a particular media mode or Assisted Telephony request mode and, if so, its position in the priority list.
old-location: tapi2\linegetapppriority.htm
tech.root: tapi
ms.assetid: b1e402b5-a2d0-444c-83c5-12782772a4b1
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: "_tapi2_linegetapppriority, lineGetAppPriority, lineGetAppPriority function [TAPI 2.2], lineGetAppPriorityA, lineGetAppPriorityW, tapi/lineGetAppPriority, tapi/lineGetAppPriorityA, tapi/lineGetAppPriorityW, tapi2.linegetapppriority"
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
req.unicode-ansi: lineGetAppPriorityW (Unicode) and lineGetAppPriorityA (ANSI)
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
 - lineGetAppPriority
 - lineGetAppPriorityA
 - lineGetAppPriorityW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineGetAppPriority function


## -description


The 
<b>lineGetAppPriority</b> function enables an application to determine whether or not it is in the handoff priority list for a particular media mode or Assisted Telephony request mode and, if so, its position in the priority list.


## -parameters




### -param lpszAppFilename

A pointer to a string that contains the application executable module file name, without directory data. In API version 2.0 or later, the parameter can be in long file name format, of which the 8.3 file name format is a proper subset. Long file names, unlike 8.3 file names, are case preserving. Neither file name format is case sensitive. For more information, see 
<a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">File Name Conventions</a>. In API versions earlier than 2.0, the parameter must specify a file name in the 8.3 format; long file names cannot be used.


### -param dwMediaMode

A media mode for which the priority data is to be obtained. The value can be one of the 
<a href="https://msdn.microsoft.com/cbb758be-3ecd-4ac4-b1b5-57136a1aad8e">LINEMEDIAMODE_ Constants</a>; only a single bit can be on. The value 0 should be used if verifying application priority for Assisted Telephony requests.


### -param lpExtensionID

A pointer to structure of type 
<a href="https://msdn.microsoft.com/bf7d9ccc-3f80-4e54-bcc2-cc2fef1d24af">LINEEXTENSIONID</a>. This parameter is ignored.


### -param dwRequestMode

The conditions for this parameter are, if the <i>dwMediaMode</i> parameter is zero, this parameter specifies the Assisted Telephony request mode for which priority is to be checked. It must be LINEREQUESTMODE_MAKECALL. This parameter is ignored if <i>dwMediaMode</i> is non-zero.


### -param lpExtensionName

This parameter is ignored.


### -param lpdwPriority

A pointer to a <b>DWORD</b>-size memory location into which TAPI writes the priority of the application for the specified media or request mode. The value 0 is returned if the application is not in the stored priority list and does not currently have any line device open with ownership requested of the specified media mode or having registered for the specified request mode. 




In API versions earlier than 2.0, the value –1 (0xFFFFFFFF) is returned if the application has the line open for the specified media mode or has registered for the specified requests, but the application is not in the stored priority list; that is, it is in the temporary priority list only. In API version 2.0 or later, the value 0 is returned to indicate this condition.

Otherwise, the value indicates the application position in the list; 1 being highest priority, and increasing values indicating decreasing priority.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

<b>LINEERR_INIFILECORRUPT</b>, <b>LINEERR_INVALREQUESTMODE</b>, <b>LINEERR_INVALAPPNAME</b>, <b>LINEERR_NOMEM</b>, <b>LINEERR_INVALMEDIAMODE</b>, <b>LINEERR_OPERATIONFAILED</b>, <b>LINEERR_INVALPOINTER</b>, <b>LINEERR_STRUCTURETOOSMALL</b>.




## -remarks



If LINEERR_INVALMEDIAMODE is returned, the value specified in <i>dwMediaMode</i> is not zero, not a valid extended media mode, and not one of the 
<a href="https://msdn.microsoft.com/cbb758be-3ecd-4ac4-b1b5-57136a1aad8e">LINEMEDIAMODE_ Constants</a>, or more than one bit is on in the parameter value.




## -see-also




<a href="https://msdn.microsoft.com/bf7d9ccc-3f80-4e54-bcc2-cc2fef1d24af">LINEEXTENSIONID</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a>
 

 

