---
UID: NF:iscsidsc.GetDevicesForIScsiSessionA
title: GetDevicesForIScsiSessionA function
author: windows-sdk-content
description: GetDevicesForIscsiSession function retrieves information about the devices associated with the current session.
old-location: iscsidisc\getdevicesforiscsisession.htm
old-project: iSCSIDisc
ms.assetid: f7a07f36-1c3b-4e33-ac6e-d2e7e8f2466a
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: GetDevicesForIScsiSessionA, GetDevicesForIscsiSession, GetDevicesForIscsiSession function [iSCSI Discovery Library API], GetDevicesForIscsiSessionA, GetDevicesForIscsiSessionW, iscsidisc.getdevicesforiscsisession, iscsidsc/GetDevicesForIscsiSession, iscsidsc/GetDevicesForIscsiSessionA, iscsidsc/GetDevicesForIscsiSessionW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: TARGET_INFORMATION_CLASS, *PTARGET_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iscsidsc.dll
api_name:
-	GetDevicesForIscsiSession
-	GetDevicesForIscsiSessionA
-	GetDevicesForIscsiSessionW
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetDevicesForIScsiSessionA function


## -description


The <b>GetDevicesForIscsiSession</b> function retrieves information about the devices associated with the current session.



## -parameters




### -param UniqueSessionId [in]

A pointer to a structure of type <a href="https://msdn.microsoft.com/d13975f9-58d0-425c-a2de-a0d1d70850d3">ISCSI_UNIQUE_SESSION_ID</a> that contains the session identifier for the session. 


### -param DeviceCount [in, out]

A pointer to a location that, on input, contains the number of elements of type <a href="https://msdn.microsoft.com/ea5d01ee-64c7-43bb-8945-af38d06de36c">ISCSI_DEVICE_ON_SESSION</a> that can fit in the buffer that <i>Devices</i> points to. If the operation succeeds, the location receives the number of elements retrieved. If <b>GetDevicesForIscsiSession</b> returns ERROR_INSUFFICIENT_BUFFER, the location still receives the number of elements the buffer is capable of containing. 


### -param Devices [out]

An array of <a href="https://msdn.microsoft.com/ea5d01ee-64c7-43bb-8945-af38d06de36c">ISCSI_DEVICE_ON_SESSION</a>-type structures that, on output, receives information about each device associated with the session. 


## -returns



Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the caller allocated insufficient buffer space for the array in Devices. 

Otherwise, <b>GetDevicesForIscsiSession</b> returns the appropriate Win32 or iSCSI error code on failure.




## -see-also




<a href="https://msdn.microsoft.com/ea5d01ee-64c7-43bb-8945-af38d06de36c">ISCSI_DEVICE_ON_SESSION</a>



<a href="https://msdn.microsoft.com/d13975f9-58d0-425c-a2de-a0d1d70850d3">ISCSI_UNIQUE_SESSION_ID</a>
 

 

