---
UID: NF:iscsidsc.GetDevicesForIScsiSessionW
title: GetDevicesForIScsiSessionW function (iscsidsc.h)
author: windows-sdk-content
description: GetDevicesForIscsiSession function retrieves information about the devices associated with the current session.
old-location: iscsidisc\getdevicesforiscsisession.htm
tech.root: iSCSIDisc
ms.assetid: f7a07f36-1c3b-4e33-ac6e-d2e7e8f2466a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDevicesForIScsiSessionW, GetDevicesForIscsiSession, GetDevicesForIscsiSession function [iSCSI Discovery Library API], GetDevicesForIscsiSessionA, GetDevicesForIscsiSessionW, iscsidisc.getdevicesforiscsisession, iscsidsc/GetDevicesForIscsiSession, iscsidsc/GetDevicesForIscsiSessionA, iscsidsc/GetDevicesForIscsiSessionW
ms.topic: function
f1_keywords: ["iscsidsc/GetDevicesForIscsiSession"]
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetDevicesForIscsiSessionW (Unicode) and GetDevicesForIscsiSessionA (ANSI)
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
 - GetDevicesForIscsiSession
 - GetDevicesForIscsiSessionA
 - GetDevicesForIscsiSessionW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetDevicesForIScsiSessionW function


## -description


The <b>GetDevicesForIscsiSession</b> function retrieves information about the devices associated with the current session.



## -parameters




### -param UniqueSessionId [in]

A pointer to a structure of type <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-_iscsi_unique_session_id">ISCSI_UNIQUE_SESSION_ID</a> that contains the session identifier for the session. 


### -param DeviceCount [in, out]

A pointer to a location that, on input, contains the number of elements of type <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_device_on_sessiona">ISCSI_DEVICE_ON_SESSION</a> that can fit in the buffer that <i>Devices</i> points to. If the operation succeeds, the location receives the number of elements retrieved. If <b>GetDevicesForIscsiSession</b> returns ERROR_INSUFFICIENT_BUFFER, the location still receives the number of elements the buffer is capable of containing. 


### -param Devices [out]

An array of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_device_on_sessiona">ISCSI_DEVICE_ON_SESSION</a>-type structures that, on output, receives information about each device associated with the session. 


## -returns



Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the caller allocated insufficient buffer space for the array in Devices. 

Otherwise, <b>GetDevicesForIscsiSession</b> returns the appropriate Win32 or iSCSI error code on failure.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_device_on_sessiona">ISCSI_DEVICE_ON_SESSION</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-_iscsi_unique_session_id">ISCSI_UNIQUE_SESSION_ID</a>
 

 

