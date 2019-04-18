---
UID: NE:rdpencomapi.__MIDL___MIDL_itf_rdpencomapi_0000_0000_0008
title: RDPSRAPI_APP_FLAGS (rdpencomapi.h)
author: windows-sdk-content
description: Defines values for the type of application.
old-location: rdp\rdpsrapi_app_flags.htm
tech.root: rdp
ms.assetid: fc7b6be3-3929-4b88-9899-3949706e8985
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: APP_FLAG_PRIVILEGED, RDPSRAPI_APP_FLAGS, RDPSRAPI_APP_FLAGS enumeration [RDP], rdp.rdpsrapi_app_flags, rdpencomapi/APP_FLAG_PRIVILEGED, rdpencomapi/RDPSRAPI_APP_FLAGS
ms.topic: enum
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rdpencomapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rdpencomapi.h
api_name:
 - RDPSRAPI_APP_FLAGS
product: Windows
targetos: Windows
req.typenames: RDPSRAPI_APP_FLAGS
req.redist: 
ms.custom: 19H1
---

# RDPSRAPI_APP_FLAGS enumeration


## -description


Defines values for the type of  application.  You can retrieve these flags  from the <a href="https://msdn.microsoft.com/9a934718-1eea-4406-a1da-b7d493f6667e">IRDPSRAPIApplication</a> interface that represents each application.

You can retrieve the list of applications that are running on the sharing user session  for both the sharer and the viewer through the <a href="https://msdn.microsoft.com/6a08c948-1b25-4a36-93c8-23e7e3f4fb08">IRDPSRAPIApplicationFilter</a> interface by calling the <a href="https://msdn.microsoft.com/08704192-320d-44f2-a811-f8565285bd30">get_Applications</a> method.


## -enum-fields




### -field APP_FLAG_PRIVILEGED

This flag indicates that the application cannot be shared. The application runs at a higher level than the process that is using the Windows Desktop Sharing API. An application can use this flag to prevent the user from sharing it by either disabling the entry for the application in the user interface or by not showing the entry.

