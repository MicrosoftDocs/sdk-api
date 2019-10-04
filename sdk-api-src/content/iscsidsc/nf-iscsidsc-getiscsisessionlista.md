---
UID: NF:iscsidsc.GetIScsiSessionListA
title: GetIScsiSessionListA function (iscsidsc.h)
author: windows-sdk-content
description: GetIscsiSessionList function retrieves the list of active iSCSI sessions.
old-location: iscsidisc\getiscsisessionlist.htm
tech.root: iSCSIDisc
ms.assetid: b16b9e52-67af-4745-ac67-a2096dafe94e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetIScsiSessionListA, GetIscsiSessionList, GetIscsiSessionList function [iSCSI Discovery Library API], GetIscsiSessionListA, GetIscsiSessionListW, iscsidisc.getiscsisessionlist, iscsidsc/GetIscsiSessionList, iscsidsc/GetIscsiSessionListA, iscsidsc/GetIscsiSessionListW
ms.topic: function
f1_keywords: 
 - "iscsidsc/GetIscsiSessionList"
dev_langs:
 - c++
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetIscsiSessionListW (Unicode) and GetIscsiSessionListA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iscsidsc.dll
api_name:
 - GetIscsiSessionList
 - GetIscsiSessionListA
 - GetIscsiSessionListW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetIScsiSessionListA function


## -description


The <b>GetIscsiSessionList</b> function retrieves the list of active iSCSI sessions.



## -parameters




### -param BufferSize [in, out]

A pointer to a location that, on input, contains the size, in bytes, of the caller-allocated buffer that <i>SessionInfo</i> points to. If the operation succeeds, the location receives the size, in bytes, of the session information data that was retrieved. 

If the operation fails because the output buffer size was insufficient, the location receives the size, in bytes, of the buffer size required to contain the output data.


### -param SessionCount [out]

A pointer to a location that, on input, contains the number of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_session_infoa">ISCSI_SESSION_INFO</a> structures that the buffer that <i>SessionInfo</i> points to can contain. If the operation succeeds, the location receives the number of <b>ISCSI_SESSION_INFO</b> structures that were retrieved.


### -param SessionInfo [out]

A pointer to a buffer that contains a series of contiguous structures of type <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_session_infoa">ISCSI_SESSION_INFO</a> that describe the active login sessions. 



## -returns



Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the size of the buffer at <i>SessionInfo</i> was insufficient to hold the output data. 

Otherwise, <b>GetIscsiSessionList</b> returns the appropriate Win32 or iSCSI error code on failure.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_session_infoa">ISCSI_SESSION_INFO</a>
 

 

