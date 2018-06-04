---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _PubAppInfo structure


## -description


Provides information about a published application from an application publisher to <b>Add/Remove Programs</b> in Control Panel.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

A value of type <b>DWORD</b> that specifies the size of the structure. This member is set by the <b>Add/Remove Programs</b> utility.


### -field dwMask

Type: <b>DWORD</b>

A bitmask that indicates which items in the structure are valid. This member can contain one or more <a href="https://msdn.microsoft.com/9fcb93a5-24b5-4bc3-9f20-0088affb183b">PUBAPPINFOFLAGS</a>.


### -field pszSource

Type: <b>LPWSTR</b>

A pointer to a string containing the display name of the publisher. This name appears in <b>Add/Remove Programs</b> if duplicate application names are encountered. The string buffer must be allocated using the Shell task allocator.


### -field stAssigned

Type: <b><a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a></b>

The time when an application manager schedules the application installation.  <b>Add/Remove Programs</b> does not allow the user to schedule an installation time later than the value in this member. This member is ignored if it describes a time prior to the current time.


### -field stPublished

Type: <b><a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a></b>


### -field stScheduled

Type: <b><a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a></b>

The installation time that the user sets by clicking <b>Add Later</b>. <b>Add/Remove Programs</b> calls the <a href="https://msdn.microsoft.com/6d8c5720-b48f-4268-810c-c04b14d20d73">IPublishedApp::Install</a> method with the <i>pInstallTime</i> parameter pointing to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the time the user entered. The application publisher maintains this value for installation scheduling. <a href="https://msdn.microsoft.com/4ffcc30a-cf07-45e7-b9a5-342fe2b553c8">IPublishedApp::GetPublishedAppInfo</a> returns the scheduled installation time in this member if the scheduled time has not been canceled using <a href="https://msdn.microsoft.com/c0d5a8cb-d382-4d7a-8d09-2dd153c03294">IPublishedApp::Unschedule</a>.


### -field stExpire

Type: <b><a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a></b>

The time after which you cannot install the published application using <b>Add/Remove Programs</b>.


## -see-also




<a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a>
 

 

