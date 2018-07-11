---
UID: NF:evntcons.EventAccessRemove
title: EventAccessRemove function
author: windows-sdk-content
description: Removes the permissions defined in the registry for the specified provider or session.
old-location: etw\eventaccessremove_func.htm
old-project: etw
ms.assetid: 9f25f163-046c-41b0-82f9-0b214b74b87e
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: EventAccessRemove, EventAccessRemove function [ETW], base.eventaccessremove_func, etw.eventaccessremove_func, evntcons/EventAccessRemove
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: evntcons.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: EVENTSECURITYOPERATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Sechost.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvAPI32-l2-1-1.dll
 - API-MS-Win-Eventing-Controller-l1-1-0.dll
 - KernelBase.dll
api_name:
 - EventAccessRemove
product: Windows
targetos: Windows
req.lib: Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008 and Windows Vista
req.dll: Sechost.dll on Windows 8.1 and Windows Server 2012; Advapi32.dll on Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008 and Windows Vista
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EventAccessRemove function


## -description


Removes the permissions defined in the registry for the specified provider or session.


## -parameters




### -param Guid [in]

GUID that uniquely identifies the provider or session whose permissions you want to remove from the 
      registry.


## -returns



Returns ERROR_SUCCESS if successful.




## -remarks



After removing the permission from the registry, the default permissions apply to the provider or session. For 
    details on the default permissions, see 
    <a href="https://msdn.microsoft.com/699bb165-680f-4d3b-8859-959f319ca4be">EventAccessControl</a>.




## -see-also




<a href="https://msdn.microsoft.com/699bb165-680f-4d3b-8859-959f319ca4be">EventAccessControl</a>



<a href="https://msdn.microsoft.com/21c87137-0e8f-43d1-9dad-9f2b4fc591a3">EventAccessQuery</a>
 

 

